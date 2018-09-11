---
UID: NS:winnetwk._DISCDLGSTRUCTA
title: "_DISCDLGSTRUCTA"
author: windows-sdk-content
description: Used in the WNetDisconnectDialog1 function. The structure contains required information for the disconnect attempt.
old-location: wnet\discdlgstruct_str.htm
tech.root: WNet
ms.assetid: ae415815-f247-4217-a4f1-6a7ca9288890
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPDISCDLGSTRUCTA, DISCDLGSTRUCT, DISCDLGSTRUCT structure [Windows Networking (WNet)], DISCDLGSTRUCTA, DISCDLGSTRUCTW, DISC_NO_FORCE, DISC_UPDATE_PROFILE, LPDISCDLGSTRUCT, LPDISCDLGSTRUCT structure pointer [Windows Networking (WNet)], _DISCDLGSTRUCTA, _win32_discdlgstruct_str, winnetwk/DISCDLGSTRUCT, winnetwk/DISCDLGSTRUCTA, winnetwk/DISCDLGSTRUCTW, winnetwk/LPDISCDLGSTRUCT, wnet.discdlgstruct_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DISCDLGSTRUCTW (Unicode) and DISCDLGSTRUCTA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnetwk.h
api_name:
 - DISCDLGSTRUCT
 - DISCDLGSTRUCTA
 - DISCDLGSTRUCTW
product: Windows
targetos: Windows
req.typenames: DISCDLGSTRUCTA, *LPDISCDLGSTRUCTA
req.redist: 
---

# _DISCDLGSTRUCTA structure


## -description


The
				<b>DISCDLGSTRUCT</b> structure is used in the 
<a href="https://msdn.microsoft.com/ec3abf0c-2a18-4d7d-aac4-e086d00fa6fe">WNetDisconnectDialog1</a> function. The structure contains required information for the disconnect attempt.


## -struct-fields




### -field cbStructure

Type: <b>DWORD</b>

The size, in bytes, of the 
<b>DISCDLGSTRUCT</b> structure. The caller must supply this value.


### -field hwndOwner

Type: <b>HWND</b>

A handle to the owner window of the dialog box.


### -field lpLocalName

Type: <b>LPTSTR</b>

A pointer to a <b>NULL</b>-terminated  string that specifies the local device name that is redirected to the network resource, such as "F:" or "LPT1".


### -field lpRemoteName

Type: <b>LPTSTR</b>

A pointer to a <b>NULL</b>-terminated  string that specifies the name of the network resource to disconnect. This member can be NULL if the <b>lpLocalName</b> member is specified. When <b>lpLocalName</b> is specified, the connection to the network resource redirected from <b>lpLocalName</b>  is disconnected.


### -field dwFlags

Type: <b>DWORD</b>

A set of bit flags describing the connection. This member can be a combination of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DISC_UPDATE_PROFILE"></a><a id="disc_update_profile"></a><dl>
<dt><b>DISC_UPDATE_PROFILE</b></dt>
</dl>
</td>
<td width="60%">
If this value is set, the specified connection is no longer a persistent one (automatically restored every time the user logs on). This flag is valid only if the <b>lpLocalName</b> member specifies a local device.

</td>
</tr>
<tr>
<td width="40%"><a id="DISC_NO_FORCE"></a><a id="disc_no_force"></a><dl>
<dt><b>DISC_NO_FORCE</b></dt>
</dl>
</td>
<td width="60%">
If this value is not set, the system applies force when attempting to disconnect from the network resource. 




This situation typically occurs when the user has files open over the connection. This value means that the user will be informed if there are open files on the connection, and asked if he or she still wants to disconnect. If the user wants to proceed, the disconnect procedure re-attempts with additional force.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/ec3abf0c-2a18-4d7d-aac4-e086d00fa6fe">WNetDisconnectDialog1</a>



<a href="https://msdn.microsoft.com/7668ac55-7104-4ddb-88eb-920cfe4e36fd">Windows Networking (WNet) Overview</a>



<a href="https://msdn.microsoft.com/7969ccbb-d1ae-4a1f-8b9c-862cc6ddef1a">Windows Networking Structures</a>
 

 

