# God-wallate-
God wallate 
import React from 'react';
import { View, Text, StyleSheet, TouchableOpacity, ScrollView, SafeAreaView } from 'react-native';
import { Ionicons, FontAwesome5 } from '@expo/vector-icons';

const GodWalletHome = () => {
  return (
    <SafeAreaView style={styles.container}>
      {/* Header Section */}
      <View style={styles.header}>
        <Text style={styles.logoText}>God Wallet</Text>
        <View style={styles.headerIcons}>
          <Ionicons name="wallet-outline" size={28} color="#FFD700" style={{marginRight: 15}} />
          <Ionicons name="notifications-outline" size={28} color="#FFD700" style={{marginRight: 15}} />
          <Ionicons name="menu-outline" size={32} color="#FFD700" />
        </View>
      </View>

      <ScrollView contentContainerStyle={styles.scrollContent}>
        {/* Balance Card */}
        <View style={styles.balanceCard}>
          <Text style={styles.label}>Current Balance</Text>
          <Text style={styles.balance}>₹ 12,456.78</Text>
          <View style={styles.buttonRow}>
            <TouchableOpacity style={styles.actionBtn}><Text style={styles.btnText}>Deposit</Text></TouchableOpacity>
            <TouchableOpacity style={styles.actionBtn}><Text style={styles.btnText}>Withdraw</Text></TouchableOpacity>
          </View>
        </View>

        {/* Featured Live Posts Section */}
        <Text style={styles.sectionTitle}>Featured Live Posts</Text>
        <View style={styles.postCard}>
          <View style={styles.imagePlaceholder}><Text style={styles.goldText}>Post Image</Text></View>
          <View style={styles.postInfo}>
            <Text style={styles.postTitle}>Golden Investment Tips</Text>
            <Text style={styles.liveBadge}>● LIVE</Text>
          </View>
        </View>

        {/* Portfolio Stats */}
        <View style={styles.statsContainer}>
          <View style={styles.statBox}>
            <Text style={styles.statLabel}>Available Post</Text>
            <Text style={styles.statValue}>7 Available</Text>
          </View>
          <View style={styles.statBox}>
            <Text style={styles.statLabel}>Total Profit</Text>
            <Text style={[styles.statValue, {color: '#4CAF50'}]}>₹ 15,200 (+30.4%)</Text>
          </View>
        </View>
      </ScrollView>

      {/* Bottom Navigation Bar */}
      <View style={styles.bottomNav}>
        <TouchableOpacity style={styles.navItem}><Ionicons name="home" size={24} color="#FFD700" /><Text style={styles.navText}>Home</Text></TouchableOpacity>
        <TouchableOpacity style={styles.navItem}><Ionicons name="radio" size={24} color="#aaa" /><Text style={styles.navText}>Live Post</Text></TouchableOpacity>
        <TouchableOpacity style={styles.plusIcon}><Ionicons name="add" size={40} color="#1a2a40" /></TouchableOpacity>
        <TouchableOpacity style={styles.navItem}><Ionicons name="checkmark-circle" size={24} color="#aaa" /><Text style={styles.navText}>Complete</Text></TouchableOpacity>
        <TouchableOpacity style={styles.navItem}><Ionicons name="person" size={24} color="#aaa" /><Text style={styles.navText}>Profile</Text></TouchableOpacity>
      </View>
    </SafeAreaView>
  );
};

const styles = StyleSheet.create({
  container: { flex: 1, backgroundColor: '#0f172a' },
  header: { flexDirection: 'row', justifyContent: 'space-between', padding: 20, alignItems: 'center' },
  logoText: { color: '#FFD700', fontSize: 24, fontWeight: 'bold' },
  headerIcons: { flexDirection: 'row', alignItems: 'center' },
  scrollContent: { padding: 20 },
  balanceCard: { backgroundColor: '#1e293b', borderRadius: 15, padding: 25, borderWeight: 1, borderColor: '#FFD700', alignItems: 'center', marginBottom: 25, shadowColor: '#FFD700', shadowOpacity: 0.2, elevation: 5 },
  label: { color: '#ccc', fontSize: 14 },
  balance: { color: '#FFD700', fontSize: 32, fontWeight: 'bold', marginVertical: 10 },
  buttonRow: { flexDirection: 'row', marginTop: 15 },
  actionBtn: { backgroundColor: 'rgba(255, 215, 0, 0.1)', paddingHorizontal: 25, paddingVertical: 10, borderRadius: 20, marginHorizontal: 10, borderWidth: 1, borderColor: '#FFD700' },
  btnText: { color: '#FFD700', fontWeight: '600' },
  sectionTitle: { color: '#FFD700', fontSize: 18, marginBottom: 15, fontWeight: 'bold' },
  postCard: { backgroundColor: '#1e293b', borderRadius: 12, overflow: 'hidden', marginBottom: 20 },
  imagePlaceholder: { height: 150, backgroundColor: '#334155', justifyContent: 'center', alignItems: 'center' },
  postInfo: { padding: 15, flexDirection: 'row', justifyContent: 'space-between' },
  postTitle: { color: '#fff', fontSize: 16 },
  liveBadge: { color: '#ff4d4d', fontWeight: 'bold' },
  statsContainer: { flexDirection: 'row', justifyContent: 'space-between' },
  statBox: { backgroundColor: '#1e293b', padding: 15, borderRadius: 12, width: '48%', borderWidth: 1, borderColor: '#334155' },
  statLabel: { color: '#aaa', fontSize: 12 },
  statValue: { color: '#fff', fontSize: 16, marginTop: 5, fontWeight: 'bold' },
  bottomNav: { flexDirection: 'row', backgroundColor: '#1e293b', height: 70, justifyContent: 'space-around', alignItems: 'center', borderTopWidth: 1, borderColor: '#334155' },
  navItem: { alignItems: 'center' },
  navText: { color: '#aaa', fontSize: 10, marginTop: 4 },
  plusIcon: { backgroundColor: '#FFD700', width: 60, height: 60, borderRadius: 30, justifyContent: 'center', alignItems: 'center', marginTop: -35, elevation: 10 },
  goldText: { color: '#FFD700' }
});

export default GodWalletHome;
