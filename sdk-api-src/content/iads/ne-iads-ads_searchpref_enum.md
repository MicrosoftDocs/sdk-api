---
UID: NE:iads.__MIDL___MIDL_itf_ads_0000_0000_0025
title: ADS_SEARCHPREF_ENUM (iads.h)
description: Specifies preferences for an IDirectorySearch object.
helpviewer_keywords: ["ADS_SEARCHPREF","ADS_SEARCHPREF_ASYNCHRONOUS","ADS_SEARCHPREF_ATTRIBTYPES_ONLY","ADS_SEARCHPREF_ATTRIBUTE_QUERY","ADS_SEARCHPREF_CACHE_RESULTS","ADS_SEARCHPREF_CHASE_REFERRALS","ADS_SEARCHPREF_DEREF_ALIASES","ADS_SEARCHPREF_DIRSYNC","ADS_SEARCHPREF_DIRSYNC_FLAG","ADS_SEARCHPREF_ENUM","ADS_SEARCHPREF_ENUM enumeration [ADSI]","ADS_SEARCHPREF_EXTENDED_DN","ADS_SEARCHPREF_PAGED_TIME_LIMIT","ADS_SEARCHPREF_PAGESIZE","ADS_SEARCHPREF_SEARCH_SCOPE","ADS_SEARCHPREF_SECURITY_MASK","ADS_SEARCHPREF_SIZE_LIMIT","ADS_SEARCHPREF_SORT_ON","ADS_SEARCHPREF_TIMEOUT","ADS_SEARCHPREF_TIME_LIMIT","ADS_SEARCHPREF_TOMBSTONE","ADS_SEARCHPREF_VLV","_ds_ads_searchpref_enum","adsi.ads__searchpref__enum","adsi.ads_searchpref_enum","iads/ADS_SEARCHPREF_ASYNCHRONOUS","iads/ADS_SEARCHPREF_ATTRIBTYPES_ONLY","iads/ADS_SEARCHPREF_ATTRIBUTE_QUERY","iads/ADS_SEARCHPREF_CACHE_RESULTS","iads/ADS_SEARCHPREF_CHASE_REFERRALS","iads/ADS_SEARCHPREF_DEREF_ALIASES","iads/ADS_SEARCHPREF_DIRSYNC","iads/ADS_SEARCHPREF_DIRSYNC_FLAG","iads/ADS_SEARCHPREF_ENUM","iads/ADS_SEARCHPREF_EXTENDED_DN","iads/ADS_SEARCHPREF_PAGED_TIME_LIMIT","iads/ADS_SEARCHPREF_PAGESIZE","iads/ADS_SEARCHPREF_SEARCH_SCOPE","iads/ADS_SEARCHPREF_SECURITY_MASK","iads/ADS_SEARCHPREF_SIZE_LIMIT","iads/ADS_SEARCHPREF_SORT_ON","iads/ADS_SEARCHPREF_TIMEOUT","iads/ADS_SEARCHPREF_TIME_LIMIT","iads/ADS_SEARCHPREF_TOMBSTONE","iads/ADS_SEARCHPREF_VLV"]
old-location: adsi\ads_searchpref_enum.htm
tech.root: adsi
ms.assetid: f3ab3d53-e53c-459e-929f-f2a3fc95c3ff
ms.date: 12/05/2018
ms.keywords: ADS_SEARCHPREF, ADS_SEARCHPREF_ASYNCHRONOUS, ADS_SEARCHPREF_ATTRIBTYPES_ONLY, ADS_SEARCHPREF_ATTRIBUTE_QUERY, ADS_SEARCHPREF_CACHE_RESULTS, ADS_SEARCHPREF_CHASE_REFERRALS, ADS_SEARCHPREF_DEREF_ALIASES, ADS_SEARCHPREF_DIRSYNC, ADS_SEARCHPREF_DIRSYNC_FLAG, ADS_SEARCHPREF_ENUM, ADS_SEARCHPREF_ENUM enumeration [ADSI], ADS_SEARCHPREF_EXTENDED_DN, ADS_SEARCHPREF_PAGED_TIME_LIMIT, ADS_SEARCHPREF_PAGESIZE, ADS_SEARCHPREF_SEARCH_SCOPE, ADS_SEARCHPREF_SECURITY_MASK, ADS_SEARCHPREF_SIZE_LIMIT, ADS_SEARCHPREF_SORT_ON, ADS_SEARCHPREF_TIMEOUT, ADS_SEARCHPREF_TIME_LIMIT, ADS_SEARCHPREF_TOMBSTONE, ADS_SEARCHPREF_VLV, _ds_ads_searchpref_enum, adsi.ads__searchpref__enum, adsi.ads_searchpref_enum, iads/ADS_SEARCHPREF_ASYNCHRONOUS, iads/ADS_SEARCHPREF_ATTRIBTYPES_ONLY, iads/ADS_SEARCHPREF_ATTRIBUTE_QUERY, iads/ADS_SEARCHPREF_CACHE_RESULTS, iads/ADS_SEARCHPREF_CHASE_REFERRALS, iads/ADS_SEARCHPREF_DEREF_ALIASES, iads/ADS_SEARCHPREF_DIRSYNC, iads/ADS_SEARCHPREF_DIRSYNC_FLAG, iads/ADS_SEARCHPREF_ENUM, iads/ADS_SEARCHPREF_EXTENDED_DN, iads/ADS_SEARCHPREF_PAGED_TIME_LIMIT, iads/ADS_SEARCHPREF_PAGESIZE, iads/ADS_SEARCHPREF_SEARCH_SCOPE, iads/ADS_SEARCHPREF_SECURITY_MASK, iads/ADS_SEARCHPREF_SIZE_LIMIT, iads/ADS_SEARCHPREF_SORT_ON, iads/ADS_SEARCHPREF_TIMEOUT, iads/ADS_SEARCHPREF_TIME_LIMIT, iads/ADS_SEARCHPREF_TOMBSTONE, iads/ADS_SEARCHPREF_VLV
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ADS_SEARCHPREF_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0000_0000_0025
 - iads/__MIDL___MIDL_itf_ads_0000_0000_0025
 - ADS_SEARCHPREF_ENUM
 - iads/ADS_SEARCHPREF_ENUM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_SEARCHPREF_ENUM
---

# ADS_SEARCHPREF_ENUM enumeration


## -description

The <b>ADS_SEARCHPREF_ENUM</b> enumeration specifies preferences for an <a href="/windows/desktop/api/iads/nn-iads-idirectorysearch">IDirectorySearch</a> object. This enumeration is used in the <b>dwSearchPref</b> member of the <a href="/windows/desktop/api/iads/ns-iads-ads_searchpref_info">ADS_SEARCHPREF_INFO</a> structure in the <a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference">IDirectorySearch::SetSearchPreference</a> method.

## -enum-fields

### -field ADS_SEARCHPREF_ASYNCHRONOUS:0

Specifies that searches should be performed asynchronously. By default, searches are synchronous.

In a synchronous search, the <a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-getfirstrow">IDirectorySearch::GetFirstRow</a> and <a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextrow">IDirectorySearch::GetNextRow</a> methods do not return until the server returns the entire result, or for a paged search, the entire page.

An asynchronous search blocks until one row of the search results is available, or until the timeout interval specified by the <b>ADS_SEARCHPREF_TIMEOUT</b> search preference elapses.

### -field ADS_SEARCHPREF_DEREF_ALIASES

Specifies that aliases of found objects are to be resolved. Use the  <a href="/windows/win32/api/iads/ne-iads-ads_derefenum">ADS_DEREFENUM</a> enumeration to specify how this is performed.

### -field ADS_SEARCHPREF_SIZE_LIMIT

Specifies the size limit that the server should observe during a search. The server stops searching when the size limit is reached and returns the results accumulated to that point. If this value is zero, the size limit is determined by the directory service. The default  for this value is zero. If this value is greater than the size limit determined by the directory service, the directory service limit takes precedence.

For Active Directory, the size limit specifies the maximum number of objects to be returned by the search. Also for Active Directory, the maximum number of objects returned by a search is 1000 objects.

### -field ADS_SEARCHPREF_TIME_LIMIT

Specifies the number of seconds that the server waits for a search to complete. When the time limit is reached, the server stops searching and returns the  results accumulated to that point. If this value is zero, the timeout period is infinite. The default for this value is 120 seconds.

### -field ADS_SEARCHPREF_ATTRIBTYPES_ONLY

Indicates that the search should obtain only the name of attributes to which values are assigned.

### -field ADS_SEARCHPREF_SEARCH_SCOPE

Specifies the search scope that should be observed by the server. For more information about the appropriate settings, see the  <a href="/windows/win32/api/iads/ne-iads-ads_scopeenum">ADS_SCOPEENUM</a> enumeration.

### -field ADS_SEARCHPREF_TIMEOUT

Specifies the time limit, in seconds, that a client will wait for the server to return the result. This option is set in an <a href="/windows/desktop/api/iads/ns-iads-ads_searchpref_info">ADS_SEARCHPREF_INFO</a> structure.

### -field ADS_SEARCHPREF_PAGESIZE

Specifies the page size in a paged search. For each request by the client, the server returns, at most, the number of objects as set by the page size. When page size is set, it is unnecessary to set the size limit. If a size limit is set, then the value for page size must be less than the value for size limit. If the value for page size exceeds size limit, then the <b>ERROR_DS_SIZELIMIT_EXCEEDED</b> error is returned with the number of rows specified by size limit.

### -field ADS_SEARCHPREF_PAGED_TIME_LIMIT

Specifies the number of seconds that the server should wait for a page of search results, as opposed to the time limit for the entire search. When the time limit is reached, the server stops searching and returns the results obtained up to that point, along with a cookie that contains the data about where to resume searching. If this value is zero, the page timeout period is infinite. The default value for this limit is 120 seconds.

### -field ADS_SEARCHPREF_CHASE_REFERRALS

Specifies that referrals may be chased. If the root search is not specified in the naming context of the server or when the search results cross a naming context, for example, when you have child domains and search in the parent domain, the server sends a referral message to the client which the client can choose to ignore or chase. For more information about referral chasing, see  <a href="/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum">ADS_CHASE_REFERRALS_ENUM</a>.

### -field ADS_SEARCHPREF_SORT_ON

Specifies that the server sorts the result set. Use the  <a href="/windows/desktop/api/iads/ns-iads-ads_sortkey">ADS_SORTKEY</a> structure to specify the sort keys. This search preference works only for directory servers that support the LDAP control for server-side sorting. Active Directory supports the sort control, but it can impact server performance, particularly if the results set is large. Active Directory supports only a single sort key.

### -field ADS_SEARCHPREF_CACHE_RESULTS

Specifies if the result should be cached on the client side. By default, ADSI caches the result set. Disabling this option may be desirable for large result sets.

### -field ADS_SEARCHPREF_DIRSYNC

Specifies a directory synchronization (DirSync) search, which returns all changes since a specified state. In the  <a href="/windows/desktop/api/iads/ns-iads-adsvalue">ADSVALUE</a> structure, set the <b>dwType</b> member to <a href="/windows/win32/api/iads/ns-iads-ads_prov_specific">ADS_PROV_SPECIFIC</a>. The <b>ProviderSpecific</b> member is an  <b>ADS_PROV_SPECIFIC</b> structure whose <b>lpValue</b> member specifies a cookie that indicates the state from which changes are retrieved. The first time you use the DirSync control, set the <b>dwLength</b> and <b>lpValue</b> members of the <b>ADS_PROV_SPECIFIC</b> structure to zero and <b>NULL</b> respectively. After reading the results set returned by the search until  <a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextrow">IDirectorySearch::GetNextRow</a> returns <b>S_ADS_NOMORE_ROWS</b>, call  <a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn">IDirectorySearch::GetColumn</a> to retrieve the <b>ADS_DIRSYNC_COOKIE</b> attribute which contains a cookie to use in the next DirSync search. For more information, see <a href="/windows/desktop/AD/polling-for-changes-using-the-dirsync-control">Polling for Changes Using the DirSync Control</a> and <a href="/previous-versions/windows/desktop/ldap/ldap-server-dirsync-oid">LDAP_SERVER_DIRSYNC_OID</a>.

This flag cannot be combined with <b>ADS_SEARCHPREF_PAGESIZE</b>.

The caller must have the <b>SE_SYNC_AGENT_NAME</b> privilege.

### -field ADS_SEARCHPREF_TOMBSTONE

Specifies whether the search should also return deleted objects that match the search filter. When objects are deleted, Active Directory moves them to a "Deleted Objects" container. By default, deleted objects are not included in the search results. In the <a href="/windows/desktop/api/iads/ns-iads-adsvalue">ADSVALUE</a> structure, set the <b>dwType</b> member to <b>ADSTYPE_BOOLEAN</b>. To include deleted objects, set the <b>Boolean</b> member of the <b>ADSVALUE</b> structure to <b>TRUE</b>.

Not all attributes are preserved when the object is deleted. You can retrieve the <b>objectGUID</b> and <b>RDN</b> attributes. The <b>distinguishedName</b> attribute is the DN of the object in the "Deleted Objects" container, not the previous DN. The <b>isDeleted</b> attribute is <b>TRUE</b> for a deleted object. For more information, see   <a href="/windows/desktop/AD/retrieving-deleted-objects">Retrieving Deleted Objects</a>.

### -field ADS_SEARCHPREF_VLV

Specifies that the search should use the LDAP virtual list view (VLV) control. <b>ADS_SEARCHPREF_VLV</b> can be used to access both string-type and offset-type VLV searches, by setting the appropriate fields. These two options cannot be used simultaneously because it is not possible to set the VLV control to request a result set that is both located at a specific offset and follows a particular value in the sort sequence.

To perform a string search, set the <b>lpszTarget</b> field in <a href="/windows/desktop/api/iads/ns-iads-ads_vlv">ADS_VLV</a> to the string to be searched for. To perform an offset type search, set the dwOffset field in <b>ADS_VLV</b>. If you use an offset search, you must set <b>lpszTarget</b> to <b>NULL</b>.

<b>ADS_SEARCHPREF_SORT_ON</b> must be set to <b>TRUE</b> when using <b>ADS_SEARCHPREF_VLV</b>. The sort order of the search results determines the order used for the VLV search. If performing an offset-type search, the offset is used as an index into the sorted list. If performing a string-type search, the server attempts to return the first entry which is greater-than-or-equal-to the string, based on the sort order.

Caching of search results is disabled when <b>ADS_SEARCHPREF_VLV</b> is specified.

If you assign <b>ADS_SEARCHPREF_CACHE_RESULTS</b> a <b>TRUE</b>, value when using <b>ADS_SEARCHPREF_VLV</b>, <a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference">SetSearchPreference</a> will fail and return the error <b>E_ADS_BAD_PARAMETER</b>.

### -field ADS_SEARCHPREF_ATTRIBUTE_QUERY

Specifies that an attribute-scoped query search should be performed. The search is performed against those objects named in a specified attribute of the base object. The <b>vValue</b> member of the <a href="/windows/desktop/api/iads/ns-iads-ads_searchpref_info">ADS_SEARCHPREF_INFO</a> structure contains a <b>ADSTYPE_CASE_IGNORE_STRING</b> value which contains the lDAPDisplayName of attribute to search. This attribute must be a <b>ADS_DN_STRING</b> attribute. Only one attribute may be specified. Search scope is automatically set to <b>ADS_SCOPE_BASE</b> when using this preference, and attempting to set the scope otherwise will fail with the error <b>E_ADS_BAD_PARAMETER</b>. With the exception of the <b>ADS_SEARCHPREF_VLV</b> preference, all other preferences that use LDAP controls, such as <b>ADS_SEARCHPREF_DIRSYNC</b>, <b>ADS_SEARCHPREF_TOMBSTONE</b>, and so on, are not allowed when this preference is specified.

### -field ADS_SEARCHPREF_SECURITY_MASK

Specifies that the search should return security access data for the specified attributes. The <b>vValue</b> member of the <a href="/windows/desktop/api/iads/ns-iads-ads_searchpref_info">ADS_SEARCHPREF_INFO</a> structure contains an <b>ADS_INTEGER</b> value that is a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>ADS_SECURITY_INFO_OWNER</b></td>
<td>Reads the owner data.</td>
</tr>
<tr>
<td><b>ADS_SECURITY_INFO_GROUP</b></td>
<td>Reads the group data.</td>
</tr>
<tr>
<td><b>ADS_SECURITY_INFO_DACL</b></td>
<td>Reads the discretionary access-control list (DACL).</td>
</tr>
<tr>
<td><b>ADS_SECURITY_INFO_SACL</b></td>
<td>Reads the system access-control list (SACL).</td>
</tr>
</table>
 

If you read a security descriptor without explicitly specifying a security mask using <b>ADS_SEARCHPREF_SECURITY_MASK</b>, it defaults to the equivalent of <b>ADS_SECURITY_INFO_OWNER</b> | <b>ADS_SECURITY_INFO_GROUP</b> | <b>ADS_SECURITY_INFO_DACL</b>.

### -field ADS_SEARCHPREF_DIRSYNC_FLAG

Contains optional flags for use with the <b>ADS_SEARCHPREF_DIRSYNC</b> search preference. The <b>vValue</b> member of the <a href="/windows/desktop/api/iads/ns-iads-ads_searchpref_info">ADS_SEARCHPREF_INFO</a> structure contains an <b>ADSTYPE_INTEGER</b> value that is zero or a combination of one or more of the following values. For more information about the DirSync control,  see <a href="/windows/desktop/AD/polling-for-changes-using-the-dirsync-control">Polling for Changes Using the DirSync Control</a> and <a href="/previous-versions/windows/desktop/ldap/ldap-server-dirsync-oid">LDAP_SERVER_DIRSYNC_OID</a>.

<table>
<tr>
<th>Identifier</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>LDAP_DIRSYNC_OBJECT_SECURITY</b></td>
<td>1</td>
<td>If this flag is not present, the caller must have the replicate changes right. If this flag is present,
the caller requires no rights, but is only allowed to see objects and attributes which are accessible to the caller.</td>
</tr>
<tr>
<td><b>LDAP_DIRSYNC_ANCESTORS_FIRST_ORDER</b></td>
<td>2048 (0x00000800)</td>
<td>Return parent objects before child objects, when parent objects would otherwise appear later in the replication stream.</td>
</tr>
<tr>
<td><b>LDAP_DIRSYNC_PUBLIC_DATA_ONLY</b></td>
<td>8192 (0x00002000)</td>
<td>Do not return private data in the search results.</td>
</tr>
<tr>
<td><b>LDAP_DIRSYNC_INCREMENTAL_VALUES</b></td>
<td>2147483648 (0x80000000)</td>
<td>If this flag is not present, all of the values, up to a server-specified limit, in a multi-valued attribute are returned when any value changes. If this flag is present, only the changed values are returned.</td>
</tr>
</table>

### -field ADS_SEARCHPREF_EXTENDED_DN

The search should return distinguished names in Active Directory extended format. The <b>vValue</b> member of the <a href="/windows/desktop/api/iads/ns-iads-ads_searchpref_info">ADS_SEARCHPREF_INFO</a> structure contains an <b>ADSTYPE_INTEGER</b> value that contains zero if  the GUID and SID portions of the DN string should be in hex format or one if the GUID and SID portions of the DN string should be in standard format. For more information about extended distinguished names, see <a href="/previous-versions/windows/desktop/ldap/ldap-server-extended-dn-oid">LDAP_SERVER_EXTENDED_DN_OID</a>.

## -remarks

To setup a search preference, assign appropriate values to the fields of an 
     <a href="/windows/desktop/api/iads/ns-iads-ads_searchpref_info">ADS_SEARCHPREF_INFO</a> structure passed to the server. The <b>vValue</b> member of the <b>ADS_SEARCHPREF_INFO</b> structure is an <a href="/windows/desktop/api/iads/ns-iads-adsvalue">ADSVALUE</a> structure. The following list lists the <b>ADS_SEARCHPREF_ENUM</b> values, the corresponding values for the <b>dwType</b> member of the <b>ADSVALUE</b> structure, and the <b>ADSVALUE</b> member that is used for the specified type.

<table>
<tr>
<th><b>ADS_SEARCHPREF_ENUM</b> value</th>
<th><b>dwType</b> member of <a href="/windows/desktop/api/iads/ns-iads-adsvalue">ADSVALUE</a>
</th>
<th>
<a href="/windows/desktop/api/iads/ns-iads-adsvalue">ADSVALUE</a> member</th>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_ASYNCHRONOUS</b></td>
<td><b>ADSTYPE_BOOLEAN</b></td>
<td><b>Boolean</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_DEREF_ALIASES</b></td>
<td><b>ADSTYPE_INTEGER</b></td>
<td><b>Integer</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_SIZE_LIMIT</b></td>
<td><b>ADSTYPE_INTEGER</b></td>
<td><b>Integer</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_TIME_LIMIT</b></td>
<td><b>ADSTYPE_INTEGER</b></td>
<td><b>Integer</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_ATTRIBTYPES_ONLY</b></td>
<td><b>ADSTYPE_BOOLEAN</b></td>
<td><b>Boolean</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_SEARCH_SCOPE</b></td>
<td><b>ADSTYPE_INTEGER</b></td>
<td><b>Integer</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_TIMEOUT</b></td>
<td><b>ADSTYPE_INTEGER</b></td>
<td><b>Integer</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_PAGESIZE</b></td>
<td><b>ADSTYPE_INTEGER</b></td>
<td><b>Integer</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_PAGED_TIME_LIMIT</b></td>
<td><b>ADSTYPE_INTEGER</b></td>
<td><b>Integer</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_CHASE_REFERRALS</b></td>
<td><b>ADSTYPE_INTEGER</b></td>
<td><b>Integer</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_SORT_ON</b></td>
<td><b>ADSTYPE_PROV_SPECIFIC</b></td>
<td><b>ProviderSpecific</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_CACHE_RESULTS</b></td>
<td><b>ADSTYPE_BOOLEAN</b></td>
<td><b>Boolean</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_DIRSYNC</b></td>
<td><b>ADSTYPE_PROV_SPECIFIC</b></td>
<td><b>ProviderSpecific</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_TOMBSTONE</b></td>
<td><b>ADSTYPE_BOOLEAN</b></td>
<td><b>Boolean</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_VLV</b></td>
<td><b>ADSTYPE_PROV_SPECIFIC</b></td>
<td><b>ProviderSpecific</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_ATTRIBUTE_QUERY</b></td>
<td><b>ADSTYPE_CASE_IGNORE_STRING</b></td>
<td><b>CaseIgnoreString</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_SECURITY_MASK</b></td>
<td><b>ADSTYPE_INTEGER</b></td>
<td><b>Integer</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_DIRSYNC_FLAG</b></td>
<td><b>ADSTYPE_INTEGER</b></td>
<td><b>Integer</b></td>
</tr>
<tr>
<td><b>ADS_SEARCHPREF_EXTENDED_DN</b></td>
<td><b>ADSTYPE_INTEGER</b></td>
<td><b>Integer</b></td>
</tr>
</table>
 

To setup multiple preferences, use an array of <a href="/windows/desktop/api/iads/ns-iads-ads_searchpref_info">ADS_SEARCHPREF_INFO</a> structures. The member values of this enumeration are assigned to the <b>dwSearchPref</b> member of the <b>ADS_SEARCHPREF_INFO</b> structure.

All options are supported by the LDAP system provider.

Because VBScript cannot read data from a type library, VBScript applications do not recognize the symbolic constants as defined above. You should use the numerical constants, instead, to set the appropriate flags in your VBScript applications. To use the symbolic constants, as a good programming practice, explicitly declare such constants, as done here, in your VBScript applications.


#### Examples

The following code example shows how to set up search preferences using the <a href="/windows/desktop/api/iads/ns-iads-ads_searchpref_info">ADS_SEARCHPREF_INFO</a> enumeration.


```cpp
HRESULT SetSearchPreferences2(
    DWORD dwScope,// -1 indicates default: subtree.
    DWORD dwOverallTimeOut,// <=0 indicates default: no time out set.
    DWORD dwOverallSizeLimit,// <=0 indicates default: no size limit set.
    DWORD dwOverallTimeLimit,// <=0 indicates default: no time limit set.
    BOOL bCacheResult,// TRUE indicates default.
    BOOL bIsAsynchronous,// FALSE indicates default.
    DWORD dwPageSize,// <=0 indicates default.
    DWORD dwPageTimeLimit,// <=0 indicates default.
    DWORD dwChaseReferral,// <=0 indicates default.
    LPOLESTR szSortKey,// NULL indicates do not sort.
    BOOL bIsDescending,
    BOOL bReturnAttributeNamesOnly,// FALSE indicates default.
    ADS_SEARCHPREF_INFO **ppSearchPref, // Return an array of search preferences.
    DWORD *pdwSearchPrefCount
)
{
   HRESULT hr = S_OK;
   DWORD dwCountPref = 0L;
 
   // Determine size of preferences array.
   DWORD dwTotal = 11L;
 
   if(dwScope==-1)
       dwTotal--;
   if(dwOverallTimeOut<=0)
       dwTotal--;
   if(dwOverallSizeLimit<=0)
       dwTotal--;
   if(dwOverallTimeLimit<=0)
       dwTotal--;
   if(bCacheResult)
       dwTotal--;
   if(!bIsAsynchronous)
       dwTotal--;
   if(dwPageSize<=0)
       dwTotal--;
   if(dwPageTimeLimit<=0)
       dwTotal--;
   if(dwChaseReferral<=0)
       dwTotal--;
   if(!bReturnAttributeNamesOnly)
       dwTotal--;
   if (!szSortKey)
       dwTotal--;
 
   ADS_SEARCHPREF_INFO *prefInfo = new ADS_SEARCHPREF_INFO[ dwTotal ];
   ADS_SORTKEY SortKey;

    if(!prefInfo)
    {
        return E_OUTOFMEMORY;
    }
 
    //////////////////
    // Search Scope
    //////////////////
    if(dwScope>=0)
    {
        prefInfo[dwCountPref].dwSearchPref =
                         ADS_SEARCHPREF_SEARCH_SCOPE;
        prefInfo[dwCountPref].vValue.dwType = ADSTYPE_INTEGER;
        prefInfo[dwCountPref].vValue.Integer = dwScope;
        dwCountPref++;
    }
 
    //////////////////
    // Time Out
    //////////////////
    if(dwOverallTimeOut>0)
    {
       prefInfo[dwCountPref].dwSearchPref = ADS_SEARCHPREF_TIMEOUT;
       prefInfo[dwCountPref].vValue.dwType = ADSTYPE_INTEGER;
       prefInfo[dwCountPref].vValue.Integer = dwOverallTimeOut;
       dwCountPref++;
    }
 
    ///////////////
    // Size Limit
    ///////////////
    if(dwOverallSizeLimit>0)
    {
       prefInfo[dwCountPref].dwSearchPref = ADS_SEARCHPREF_SIZE_LIMIT;
       prefInfo[dwCountPref].vValue.dwType = ADSTYPE_INTEGER;
       prefInfo[dwCountPref].vValue.Integer = dwOverallSizeLimit;
       dwCountPref++;
    }
 
    ///////////////
    // Time Limit
    ///////////////
    if(dwOverallTimeLimit>0) 
    {
       prefInfo[dwCountPref].dwSearchPref = ADS_SEARCHPREF_TIME_LIMIT;
       prefInfo[dwCountPref].vValue.dwType = ADSTYPE_INTEGER;
       prefInfo[dwCountPref].vValue.Integer = dwOverallTimeLimit;
       dwCountPref++;
    }
 
    /////////////////
    // Cache Result
    /////////////////
 
    if (!bCacheResult)
    {
        prefInfo[dwCountPref].dwSearchPref =
                              ADS_SEARCHPREF_CACHE_RESULTS;
        prefInfo[dwCountPref].vValue.dwType = ADSTYPE_BOOLEAN;
        prefInfo[dwCountPref].vValue.Boolean = bCacheResult;
        dwCountPref++;
    }
 
    //////////////
    // Page Size
    //////////////
    if(dwPageSize>0)
    {
        prefInfo[dwCountPref].dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
        prefInfo[dwCountPref].vValue.dwType = ADSTYPE_INTEGER;;
        prefInfo[dwCountPref].vValue.Integer = dwPageSize;
        dwCountPref++;
    }
 
    //////////////////
    // Page Time Limit
    //////////////////
    if(dwPageTimeLimit>0)
    {
        prefInfo[dwCountPref].dwSearchPref = 
                                      ADS_SEARCHPREF_PAGED_TIME_LIMIT;
        prefInfo[dwCountPref].vValue.dwType = ADSTYPE_INTEGER;;
        prefInfo[dwCountPref].vValue.Integer = dwPageTimeLimit;
        dwCountPref++;
    }
 
    ///////////////////
    // Chase Referrals
    ///////////////////
    if(dwChaseReferral>0)
    {
        prefInfo[dwCountPref].dwSearchPref =
                                      ADS_SEARCHPREF_CHASE_REFERRALS;
        prefInfo[dwCountPref].vValue.dwType = ADSTYPE_INTEGER;
        prefInfo[dwCountPref].vValue.Integer = dwChaseReferral;
        dwCountPref++;
    }
 
    /////////////
    // Sort
    /////////////
    if (szSortKey)
    {
        prefInfo[dwCountPref].dwSearchPref = ADS_SEARCHPREF_SORT_ON;
        prefInfo[dwCountPref].vValue.dwType = ADSTYPE_PROV_SPECIFIC;
        SortKey.pszAttrType = (LPWSTR)LocalAlloc(
                        LPTR,
                        wcslen(szSortKey)*sizeof(WCHAR) +sizeof(WCHAR)
                        );
        wcscpy_s(SortKey.pszAttrType,szSortKey);
        SortKey.pszReserved = NULL;
        SortKey.fReverseorder = 0;
        prefInfo[dwCountPref].vValue.ProviderSpecific.dwLength = 
                                                 sizeof(ADS_SORTKEY);
        prefInfo[dwCountPref].vValue.ProviderSpecific.lpValue = 
                                                 (LPBYTE) &SortKey;
        dwCountPref++;
    }
    
    /////////////////
    // Asynchronous
    /////////////////
    if(bIsAsynchronous)
    {
        prefInfo[dwCountPref].dwSearchPref =
                                     ADS_SEARCHPREF_ASYNCHRONOUS;
        prefInfo[dwCountPref].vValue.dwType = ADSTYPE_BOOLEAN;
        prefInfo[dwCountPref].vValue.Integer = bIsAsynchronous;
        dwCountPref++;
    }
 
    ////////////////////////
    // Attribute Type Only
    ////////////////////////
    if(bReturnAttributeNamesOnly)
    {
        prefInfo[dwCountPref].dwSearchPref =
                                  ADS_SEARCHPREF_ATTRIBTYPES_ONLY;
        prefInfo[dwCountPref].vValue.dwType = ADSTYPE_BOOLEAN;
        prefInfo[dwCountPref].vValue.Integer = 
                                  bReturnAttributeNamesOnly;
        dwCountPref++;
    }
 
    if (SUCCEEDED(hr))
    {
        *pdwSearchPrefCount = dwCountPref;
        *ppSearchPref  = prefInfo;
    }
    else
    {
        *pdwSearchPrefCount = 0L;
        *ppSearchPref  = NULL;
    }
 
 
    return hr;
}
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-enumerations">ADSI
  Enumerations</a>



<a href="/windows/desktop/api/iads/ns-iads-adsvalue">ADSVALUE</a>



<a href="/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum">ADS_CHASE_REFERRALS_ENUM</a>



<a href="/windows/win32/api/iads/ne-iads-ads_derefenum">ADS_DEREFENUM</a>



<a href="/windows/win32/api/iads/ns-iads-ads_prov_specific">ADS_PROV_SPECIFIC</a>



<a href="/windows/win32/api/iads/ne-iads-ads_scopeenum">ADS_SCOPEENUM</a>



<a href="/windows/desktop/api/iads/ns-iads-ads_searchpref_info">ADS_SEARCHPREF_INFO</a>



<a href="/windows/desktop/api/iads/ns-iads-ads_sortkey">ADS_SORTKEY</a>



<a href="/windows/desktop/api/iads/ns-iads-ads_vlv">ADS_VLV</a>



<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn">IDirectorySearch::GetColumn</a>



<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextrow">IDirectorySearch::GetNextRow</a>



<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference">IDirectorySearch::SetSearchPreference</a>



<a href="/windows/desktop/AD/polling-for-changes-using-the-dirsync-control">Polling for Changes Using the DirSync Control</a>



<a href="/windows/desktop/AD/retrieving-deleted-objects">Retrieving
  Deleted Objects</a>
