---
UID: NF:clusapi.ClusterRegCreateKey
title: ClusterRegCreateKey function
author: windows-driver-content
description: Creates a specified cluster database key. If the key already exists in the database, ClusterRegCreateKey opens it without making changes.
old-location: mscs\clusterregcreatekey.htm
old-project: MsCS
ms.assetid: a5e924bd-9336-45c8-b2c9-48291f8db774
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: ACCESS_SYSTEM_SECURITY, ClusterRegCreateKey, ClusterRegCreateKey function [Failover Cluster], DELETE, KEY_ALL_ACCESS, KEY_CREATE_LINK, KEY_ENUMERATE_SUB_KEYS, KEY_EXECUTE, KEY_NOTIFY, KEY_QUERY_VALUE, KEY_READ, KEY_SET_VALUE, KEY_WRITE, READ_CONTROL, REG_CREATED_NEW_KEY, REG_OPENED_EXISTING_KEY, REG_OPTION_NON_VOLATILE, WRITE_DAC, WRITE_OWNER, _wolf_clusterregcreatekey, clusapi/ClusterRegCreateKey, mscs.clusterregcreatekey
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: SR_REPLICATED_DISK_TYPE, *PSR_REPLICATED_DISK_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	ClusAPI.dll
-	Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
-	Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
-	ClusterRegCreateKey
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# ClusterRegCreateKey function


## -description


Creates a specified <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> key. If the key 
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
       <a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>.



#### ACCESS_SYSTEM_SECURITY (0x01000000)

Permission to access system security. It is used to indicate access to a 
         <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL). This type of 
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
         <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> 
         (DACL) of the security descriptor.



#### WRITE_DAC (0x00040000)

Permission to write to the DACL.



#### WRITE_OWNER (0x00080000)

Permission to change the owner.


### -param lpSecurityAttributes [in, optional]

This parameter is ignored. To set the security attributes on a new registry key, call the 
       <a href="https://msdn.microsoft.com/adb2ea52-6a3a-4243-944d-c7ae68a42a1a">ClusterRegSetKeySecurity</a> function after 
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
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



Callers should call <a href="https://msdn.microsoft.com/2216ac42-6beb-4ceb-bd15-12bb2886bc6a">ClusterRegCloseKey</a> to close 
     the key handle created by the <b>ClusterRegCreateKey</b> 
     function when they are done with it.

Do not call <b>ClusterRegCreateKey</b> from the 
     following resource DLL entry point functions:

<ul>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn997350">Offline</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn997353">Online</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b53ab7db-ed17-4386-8a5f-5d0b0d1cb1b3">Terminate</a>
</li>
</ul>
<b>ClusterRegCreateKey</b> can be safely called from 
     any other resource DLL entry point function or from a worker thread. For more information, see 
     <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/2bb0650f-ef9c-40bb-ae90-229bfa23838e">Cluster Registry Access Functions</a>



<a href="https://msdn.microsoft.com/2216ac42-6beb-4ceb-bd15-12bb2886bc6a">ClusterRegCloseKey</a>



<a href="https://msdn.microsoft.com/af2b3b9c-2ff1-483e-a9cf-5db7b1fcbd85">ClusterRegDeleteKey</a>



<a href="https://msdn.microsoft.com/f2cf204e-d02d-40b9-86d7-0262b8cc4db1">ClusterRegOpenKey</a>
 

 

