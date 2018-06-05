---
UID: NS:lmaccess._NET_DISPLAY_GROUP
title: "_NET_DISPLAY_GROUP"
author: windows-sdk-content
description: The NET_DISPLAY_GROUP structure contains information that an account manager can access to determine information about group accounts.
old-location: netmgmt\net_display_group_str.htm
old-project: NetMgmt
ms.assetid: 8e467f20-2cfb-40ae-a8b2-a5350d736eed
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*PNET_DISPLAY_GROUP, NET_DISPLAY_GROUP, NET_DISPLAY_GROUP structure [Network Management], PNET_DISPLAY_GROUP, PNET_DISPLAY_GROUP structure pointer [Network Management], _NET_DISPLAY_GROUP, _win32_net_display_group_str, lmaccess/NET_DISPLAY_GROUP, lmaccess/PNET_DISPLAY_GROUP, netmgmt.net_display_group_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lmaccess.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: NET_DISPLAY_GROUP, *PNET_DISPLAY_GROUP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Lmaccess.h
api_name:
-	NET_DISPLAY_GROUP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _NET_DISPLAY_GROUP structure


## -description


The
				<b>NET_DISPLAY_GROUP</b> structure contains information that an account manager can access to determine information about group accounts.


## -struct-fields




### -field grpi3_name

Type: <b>LPWSTR</b>

A pointer to a Unicode string that specifies the name of the group.


### -field grpi3_comment

Type: <b>LPWSTR</b>

A pointer to a Unicode string that contains a comment associated with the group. This string can be a null string, or it can have any number of characters before the terminating null character.


### -field grpi3_group_id

Type: <b>DWORD</b>

The relative identifier (RID) of the group. The relative identifier is determined by the accounts database when the group is created. It uniquely identifies the group to the account manager within the domain. The 
<a href="https://msdn.microsoft.com/b5ca5f76-d40b-4abf-925a-0de54fc476e4">NetUserAdd</a> and 
<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a> functions ignore this member. For more information about RIDs, see 
<a href="https://msdn.microsoft.com/528412e7-c2b6-4ddd-86de-999252972421">SID Components</a>.


### -field grpi3_attributes

Type: <b>DWORD</b>

These attributes are hard-coded to SE_GROUP_MANDATORY, SE_GROUP_ENABLED, and SE_GROUP_ENABLED_BY_DEFAULT. For more information, see 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556834">TOKEN_GROUPS</a>. 



					


### -field grpi3_next_index

Type: <b>DWORD</b>

The index of the last entry returned by the 
<a href="https://msdn.microsoft.com/049f1ea3-4d23-4b35-8b08-7256859aed45">NetQueryDisplayInformation</a> function. Pass this value as the <i>Index</i> parameter to 
<b>NetQueryDisplayInformation</b> to return the next logical entry. Note that you should not use the value of this member for any purpose except to retrieve more data with additional calls to 
<b>NetQueryDisplayInformation</b>.


## -see-also




<a href="https://msdn.microsoft.com/9c97420d-bc8a-42c9-b7ea-3d2ebc0034b3">Get Functions</a>



<a href="https://msdn.microsoft.com/049f1ea3-4d23-4b35-8b08-7256859aed45">NetQueryDisplayInformation</a>



<a href="https://msdn.microsoft.com/b5ca5f76-d40b-4abf-925a-0de54fc476e4">NetUserAdd</a>



<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556834">TOKEN_GROUPS</a>
 

 

