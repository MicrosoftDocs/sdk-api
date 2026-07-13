---
UID: NF:clusapi.ClusterRegCreateKey
title: ClusterRegCreateKey function (clusapi.h)
description: Creates a specified cluster database key. If the key already exists in the database, ClusterRegCreateKey opens it without making changes.
helpviewer_keywords: ["ACCESS_SYSTEM_SECURITY","ClusterRegCreateKey","ClusterRegCreateKey function [Failover Cluster]","DELETE","KEY_ALL_ACCESS","KEY_CREATE_LINK","KEY_ENUMERATE_SUB_KEYS","KEY_EXECUTE","KEY_NOTIFY","KEY_QUERY_VALUE","KEY_READ","KEY_SET_VALUE","KEY_WRITE","READ_CONTROL","REG_CREATED_NEW_KEY","REG_OPENED_EXISTING_KEY","REG_OPTION_NON_VOLATILE","WRITE_DAC","WRITE_OWNER","_wolf_clusterregcreatekey","clusapi/ClusterRegCreateKey","mscs.clusterregcreatekey"]
old-location: mscs\clusterregcreatekey.htm
tech.root: MsCS
ms.assetid: a5e924bd-9336-45c8-b2c9-48291f8db774
ms.date: 12/05/2018
ms.keywords: ACCESS_SYSTEM_SECURITY, ClusterRegCreateKey, ClusterRegCreateKey function [Failover Cluster], DELETE, KEY_ALL_ACCESS, KEY_CREATE_LINK, KEY_ENUMERATE_SUB_KEYS, KEY_EXECUTE, KEY_NOTIFY, KEY_QUERY_VALUE, KEY_READ, KEY_SET_VALUE, KEY_WRITE, READ_CONTROL, REG_CREATED_NEW_KEY, REG_OPENED_EXISTING_KEY, REG_OPTION_NON_VOLATILE, WRITE_DAC, WRITE_OWNER, _wolf_clusterregcreatekey, clusapi/ClusterRegCreateKey, mscs.clusterregcreatekey
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ClusterRegCreateKey
 - clusapi/ClusterRegCreateKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-clusapi-l1-1-6.dll
 - ext-ms-win-cluster-clusapi-l1-1-5.dll
 - ext-ms-win-cluster-clusapi-l1-1-4.dll
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
api_name:
 - ClusterRegCreateKey
---

# ClusterRegCreateKey function


## -description

Creates a specified <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> key. If the key 
    already exists in the database, 
    <b>ClusterRegCreateKey</b> opens it without making 
    changes.

## -parameters

### -param hKey [in]

Handle to an open cluster database key. This parameter cannot be <b>NULL</b>.

### -param lpszSubKey [in]

Pointer to a null-terminated Unicode string specifying the name of the subkey to be created or opened. The 
       <i>lpszSubKey</i> parameter must point to a subkey that:

<ul>
<li>Is a child key of the key identified by <i>hKey</i>.</li>
<li>Must not begin with the backslash character ( \ ).</li>
<li>Must not be <b>NULL</b>.</li>
</ul>
The <i>lpszSubKey</i> parameter can point to an empty string, causing 
       <b>ClusterRegCreateKey</b> to return a handle to the 
       database key represented by <i>hKey</i>.

### -param dwOptions [in]

Specifies special options for this key. Currently, <i>dwOptions</i> can be set to the 
       following value.



#### REG_OPTION_NON_VOLATILE (0x00000000)

The opened or created key is not volatile; the information is preserved when the system is restarted.

### -param samDesired [in]

Access mask that specifies the needed security access for the new key. The following values are valid.

For more information, see 
       <a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.



#### ACCESS_SYSTEM_SECURITY (0x01000000)

Permission to access system security. It is used to indicate access to a 
         <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL). This type of 
         access requires the calling process to have the <b>SE_SECURITY_NAME</b> (Manage auditing 
         and security log) privilege.



#### DELETE (0x00010000)

Permission to delete.



#### KEY_ALL_ACCESS (0x000F003F)

Combination of <b>KEY_QUERY_VALUE</b>, <b>KEY_ENUMERATE_SUB_KEYS</b>, 
         <b>KEY_NOTIFY</b>, <b>KEY_CREATE_SUB_KEY</b>, 
         <b>KEY_CREATE_LINK</b>, and <b>KEY_SET_VALUE</b> access.



#### KEY_CREATE_LINK (0x00000020)

Permission to create a symbolic link.



#### KEY_ENUMERATE_SUB_KEYS (0x00000008)

Permission to enumerate subkeys.



#### KEY_EXECUTE (0x00020019)

Permission for read access.



#### KEY_NOTIFY (0x00000010)

Permission for change notification.



#### KEY_QUERY_VALUE (0x00000001)

Permission to query subkey data.



#### KEY_READ (0x00020019)

Combination of <b>KEY_QUERY_VALUE</b>, <b>KEY_ENUMERATE_SUB_KEYS</b>, 
         and <b>KEY_NOTIFY</b> access.



#### KEY_SET_VALUE (0x00000002)

Permission to change subkey data.



#### KEY_WRITE (0x00020006)

Combination of <b>KEY_SET_VALUE</b> and <b>KEY_CREATE_SUB_KEY</b> 
         access.



#### READ_CONTROL (0x00020000)

Permission to read the owner, group, and 
         <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> 
         (DACL) of the security descriptor.



#### WRITE_DAC (0x00040000)

Permission to write to the DACL.



#### WRITE_OWNER (0x00080000)

Permission to change the owner.

### -param lpSecurityAttributes [in, optional]

This parameter is ignored. To set the security attributes on a new registry key, call the 
       <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregsetkeysecurity">ClusterRegSetKeySecurity</a> function after 
       <b>ClusterRegCreateKey</b> has returned 
       successfully.

### -param phkResult [out]

Pointer to the handle of the opened or created key.

### -param lpdwDisposition [out, optional]

Pointer to a value that describes whether the key pointed to by <i>lpszSubKey</i> was 
       opened or created. The following values are valid.



#### REG_CREATED_NEW_KEY (0x00000001)

The key did not exist and was created.



#### REG_OPENED_EXISTING_KEY (0x00000002)

The key existed and was opened.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

Callers should call <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregclosekey">ClusterRegCloseKey</a> to close 
     the key handle created by the <b>ClusterRegCreateKey</b> 
     function when they are done with it.

Do not call <b>ClusterRegCreateKey</b> from the 
     following resource DLL entry point functions:

<ul>
<li>
<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pclose_routine">Close</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Offline</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-ponline_routine">Online</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-popen_routine">Open</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pterminate_routine">Terminate</a>
</li>
</ul>
<b>ClusterRegCreateKey</b> can be safely called from 
     any other resource DLL entry point function or from a worker thread. For more information, see 
     <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-registry-access-functions">Cluster Registry Access Functions</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregclosekey">ClusterRegCloseKey</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregdeletekey">ClusterRegDeleteKey</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregopenkey">ClusterRegOpenKey</a>