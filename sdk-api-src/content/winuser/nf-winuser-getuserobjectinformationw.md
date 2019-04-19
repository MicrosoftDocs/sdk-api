---
UID: NF:winuser.GetUserObjectInformationW
title: GetUserObjectInformationW function (winuser.h)
author: windows-sdk-content
description: Retrieves information about the specified window station or desktop object.
old-location: winstation\getuserobjectinformation.htm
tech.root: winstation
ms.assetid: 64f7361d-1a94-4d5b-86f1-a2a21737668a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetUserObjectInformation, GetUserObjectInformation function [Windows Stations and Desktops], GetUserObjectInformationA, GetUserObjectInformationW, UOI_FLAGS, UOI_HEAPSIZE, UOI_IO, UOI_NAME, UOI_TYPE, UOI_USER_SID, _win32_getuserobjectinformation, base.getuserobjectinformation, winstation.getuserobjectinformation, winuser/GetUserObjectInformation, winuser/GetUserObjectInformationA, winuser/GetUserObjectInformationW
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetUserObjectInformationW (Unicode) and GetUserObjectInformationA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-RTCore-NTUser-WindowStation-L1-1-0.dll
 - Ext-Ms-Win-NTUser-Windowstation-Ansi-L1-1-0.dll
 - Ext-MS-Win-NTUser-WindowStation-Ansi-L1-1-1.dll
 - Ext-MS-Win-NTUser-Windowstation-L1-1-0.dll
 - Ext-MS-Win-NTUser-Windowstation-L1-1-1.dll
 - Ext-MS-Win-NTUser-WindowStation-L1-1-2.dll
api_name:
 - GetUserObjectInformation
 - GetUserObjectInformationA
 - GetUserObjectInformationW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetUserObjectInformationW function


## -description


Retrieves information about the specified window station or desktop object.


## -parameters




### -param hObj [in]

A handle to the window station or desktop object. This handle is returned by the 
<a href="https://msdn.microsoft.com/c1aee546-decd-46c9-8d02-d6792f5a6a0d">CreateWindowStation</a>, 
<a href="https://msdn.microsoft.com/78ee7100-1bad-4c2d-b923-c5e67191bd41">OpenWindowStation</a>, 
<a href="https://msdn.microsoft.com/c6ed40c5-13a9-4697-a727-730adc6a912d">CreateDesktop</a>, or 
<a href="https://msdn.microsoft.com/7f805f47-1737-4f4b-a74a-9c1423b65f2c">OpenDesktop</a> function.


### -param nIndex [in]

The information to be retrieved. The parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="UOI_FLAGS"></a><a id="uoi_flags"></a><dl>
<dt><b>UOI_FLAGS</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The handle flags. The <i>pvInfo</i> parameter must point to a 
<a href="https://msdn.microsoft.com/5a973d45-5ff4-47e7-a927-72d3fdd61dc9">USEROBJECTFLAGS</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="UOI_HEAPSIZE"></a><a id="uoi_heapsize"></a><dl>
<dt><b>UOI_HEAPSIZE</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The size of the desktop heap, in KB, as a <b>ULONG</b> value. The <i>hObj</i> parameter must be  a handle to a desktop object, otherwise, the function fails.

<b>Windows Server 2003 and Windows XP/2000:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="UOI_IO"></a><a id="uoi_io"></a><dl>
<dt><b>UOI_IO</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
<b>TRUE</b> if  the <i>hObj</i> parameter is  a handle to the desktop object that is receiving input from the user. <b>FALSE</b> otherwise.

<b>Windows Server 2003 and Windows XP/2000:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="UOI_NAME"></a><a id="uoi_name"></a><dl>
<dt><b>UOI_NAME</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The name of the object, as a string.

</td>
</tr>
<tr>
<td width="40%"><a id="UOI_TYPE"></a><a id="uoi_type"></a><dl>
<dt><b>UOI_TYPE</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The type name of the object, as a string.

</td>
</tr>
<tr>
<td width="40%"><a id="UOI_USER_SID"></a><a id="uoi_user_sid"></a><dl>
<dt><b>UOI_USER_SID</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The 
<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure that identifies the user that is currently associated with the specified object. If no user is associated with the object, the value returned in the buffer pointed to by <i>lpnLengthNeeded</i> is zero. Note that <b>SID</b> is a variable length structure. You will usually make a call to 
<b>GetUserObjectInformation</b> to determine the length of the <b>SID</b> before retrieving its value.

</td>
</tr>
</table>
 


### -param pvInfo [out, optional]

A pointer to a buffer to receive the object information.


### -param nLength [in]

The size of the buffer pointed to by the <i>pvInfo</i> parameter, in bytes.


### -param lpnLengthNeeded [out, optional]

A pointer to a variable receiving the number of bytes required to store the requested information. If this variable's value is greater than the value of the <i>nLength</i> parameter when the function returns, the function returns FALSE, and none of the information is copied to the <i>pvInfo</i> buffer. If the value of the variable pointed to by <i>lpnLengthNeeded</i> is less than or equal to the value of <i>nLength</i>, the entire information block is copied.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/c6ed40c5-13a9-4697-a727-730adc6a912d">CreateDesktop</a>



<a href="https://msdn.microsoft.com/c1aee546-decd-46c9-8d02-d6792f5a6a0d">CreateWindowStation</a>



<a href="https://msdn.microsoft.com/998c2520-7833-4efd-a794-b13b528f0485">GetUserObjectSecurity</a>



<a href="https://msdn.microsoft.com/7f805f47-1737-4f4b-a74a-9c1423b65f2c">OpenDesktop</a>



<a href="https://msdn.microsoft.com/78ee7100-1bad-4c2d-b923-c5e67191bd41">OpenWindowStation</a>



<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a>



<a href="https://msdn.microsoft.com/42ce6946-1659-41a3-8ba7-21588583b4bd">SetUserObjectInformation</a>



<a href="https://msdn.microsoft.com/219e41b8-9ac7-4747-a585-b6b9df6a1c9c">SetUserObjectSecurity</a>



<a href="https://msdn.microsoft.com/5a973d45-5ff4-47e7-a927-72d3fdd61dc9">USEROBJECTFLAGS</a>



<a href="https://msdn.microsoft.com/6214c28f-1035-446c-8c79-5d1dd638af2a">Window Station and Desktop Functions</a>
 

 

