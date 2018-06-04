---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# MsiAdvertiseProductW function


## -description


The 
<b>MsiAdvertiseProduct</b> function generates an advertise script or advertises a product to the computer. The 
<b>MsiAdvertiseProduct</b> function enables the installer to write to a script the registry and shortcut information used to assign or publish a product. The script can be written to be consistent with a specified platform by using 
<a href="https://msdn.microsoft.com/27e8deb6-912f-4103-97a6-ec505340dccc">MsiAdvertiseProductEx</a>.


## -parameters




### -param szPackagePath [in]

The full path to the package of the product being advertised.


### -param szScriptfilePath [in]

The full path to script file that will be created with the advertise information. To advertise the product locally to the computer, set ADVERTISEFLAGS_MACHINEASSIGN or ADVERTISEFLAGS_USERASSIGN. 



<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ADVERTISEFLAGS_MACHINEASSIGN"></a><a id="advertiseflags_machineassign"></a><dl>
<dt><b>ADVERTISEFLAGS_MACHINEASSIGN</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Set to advertise a per-machine installation of the product available to all users.

</td>
</tr>
<tr>
<td width="40%"><a id="ADVERTISEFLAGS_USERASSIGN"></a><a id="advertiseflags_userassign"></a><dl>
<dt><b>ADVERTISEFLAGS_USERASSIGN</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Set to advertise a per-user installation of the product available to a particular user.

</td>
</tr>
</table>
 


### -param szTransforms [in]

A semicolon-delimited list of transforms to be applied. The list of transforms can be prefixed with the @ or | character to specify the secure caching of transforms. The @ prefix specifies secure-at-source transforms and the | prefix indicates secure full path transforms. For more information, see 
<a href="https://msdn.microsoft.com/c6019b28-b0a7-4104-9d78-b4b4228635b8">Secured Transforms</a>. This parameter may be null.


### -param lgidLanguage [in]

The installation language to use if the source supports multiple languages.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>An error relating to an action</b></dt>
</dl>
</td>
<td width="60%">
See 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/5cce27ff-1143-4fe6-b4bd-727581431c07">Initialization Error</a></b></dt>
</dl>
</td>
<td width="60%">
An initialization error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CALL_NOT_IMPLEMENTED</b></dt>
</dl>
</td>
<td width="60%">
This error is returned if an attempt is made to generate an advertise script on any platform other than Windows 2000 or Windows XP. Advertisement to the local computer is supported on all platforms.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c4a0f4d8-818d-4e60-908b-adaa2a54de95">Multiple-Package Installations</a>
 

 

