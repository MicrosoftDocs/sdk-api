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

# MsiGetComponentPathA function


## -description


The 
<b>MsiGetComponentPath</b> function returns the full path to an installed component. If the key path for the component is a registry key then the registry key is returned.


## -parameters




### -param szProduct [in]

Specifies the product code for the client product.


### -param szComponent [in]

Specifies the component ID of the component to be located.


### -param lpPathBuf [out]

Pointer to a variable that receives the path to the component. This parameter can be null. If the component is a registry key, the registry roots are represented numerically. If this is a registry subkey path, there is a backslash at the end of the Key Path. If this is a registry value key path, there is no backslash at the end. For example, a registry path on a 32-bit operating system of <b>HKEY_CURRENT_USER</b>\<b>SOFTWARE</b>\<b>Microsoft</b> is returned as "01:\SOFTWARE\Microsoft\". The registry roots returned on 32-bit operating systems are defined as shown in the following table. 




<div class="alert"><b>Note</b>  On 64-bit operating systems, a value of 20 is added to the numerical registry roots in this table to distinguish them from registry key paths on 32-bit operating systems.
For example, a registry key path of <b>HKEY_CURRENT_USER</b>\<b>SOFTWARE</b>\<b>Microsoft</b> is returned as "21:\SOFTWARE\Microsoft\", if the component path is a registry key on a 64-bit operating system.</div>
<div> </div>


<table>
<tr>
<th>Root</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HKEY_CLASSES_ROOT"></a><a id="hkey_classes_root"></a><dl>
<dt><b>HKEY_CLASSES_ROOT</b></dt>
</dl>
</td>
<td width="60%">
00

</td>
</tr>
<tr>
<td width="40%"><a id="HKEY_CURRENT_USER"></a><a id="hkey_current_user"></a><dl>
<dt><b>HKEY_CURRENT_USER</b></dt>
</dl>
</td>
<td width="60%">
01

</td>
</tr>
<tr>
<td width="40%"><a id="HKEY_LOCAL_MACHINE"></a><a id="hkey_local_machine"></a><dl>
<dt><b>HKEY_LOCAL_MACHINE</b></dt>
</dl>
</td>
<td width="60%">
02

</td>
</tr>
<tr>
<td width="40%"><a id="HKEY_USERS"></a><a id="hkey_users"></a><dl>
<dt><b>HKEY_USERS</b></dt>
</dl>
</td>
<td width="60%">
03

</td>
</tr>
</table>
 


### -param pcchBuf [in, out]

Pointer to a variable that specifies the size, in characters, of the buffer pointed to by the <i>lpPathBuf</i> parameter. On input, this is the full size of the buffer, including a space for a terminating null character. If the buffer passed in is too small, the count returned does not include the terminating null character. 




If <i>lpPathBuf</i> is null, <i>pcchBuf</i> can be null.


## -returns



The 
<b>MsiGetComponentPath</b> function returns the following values.
					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_NOTUSED</b></dt>
</dl>
</td>
<td width="60%">
The component being requested is disabled on the computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_ABSENT</b></dt>
</dl>
</td>
<td width="60%">
The component is not installed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the function parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
The component is installed locally.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_SOURCE</b></dt>
</dl>
</td>
<td width="60%">
The component is installed to run from source.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_SOURCEABSENT</b></dt>
</dl>
</td>
<td width="60%">
The component source is inaccessible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The product code or component ID is unknown.

</td>
</tr>
</table>
 




## -remarks



Upon success of the 
<b>MsiGetComponentPath</b> function, the <i>pcchBuf</i> parameter contains the length of the string in <i>lpPathBuf</i>.

The 
<b>MsiGetComponentPath</b> function might return INSTALLSTATE_ABSENT or INSTALL_STATE_UNKNOWN, for the following reasons:

<ul>
<li>INSTALLSTATE_ABSENT 


The application did not properly ensure that the feature was installed by calling 
<a href="https://msdn.microsoft.com/7a4dc671-d82e-4775-8198-79b80a4dd9e4">MsiUseFeature</a> and, if necessary, 
<a href="https://msdn.microsoft.com/067d6fbb-833f-4e0e-bfdb-18d1b8608f58">MsiConfigureFeature</a>.

</li>
<li>INSTALLSTATE_UNKNOWN 


The feature is not published. The application should have determined this earlier by calling 
<a href="https://msdn.microsoft.com/d84aa7f1-d29a-493d-a065-8f7b680019d7">MsiQueryFeatureState</a> or 
<a href="https://msdn.microsoft.com/0ac6fea4-cdc8-4799-9001-f9399b22e7a5">MsiEnumFeatures</a>. The application makes these calls while it initializes. An application should only use features that are known to be published. Since INSTALLSTATE_UNKNOWN should have been returned by 
<a href="https://msdn.microsoft.com/7a4dc671-d82e-4775-8198-79b80a4dd9e4">MsiUseFeature</a> as well, either 
<b>MsiUseFeature</b> was not called, or its return value was not properly checked.

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/05a16915-6b47-4d51-b62a-5a4d92b87e50">Component-Specific Functions</a>
 

 

