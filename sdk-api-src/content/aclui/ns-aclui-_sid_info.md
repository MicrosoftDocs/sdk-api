---
UID: NS:aclui._SID_INFO
title: "_SID_INFO"
author: windows-driver-content
description: Contains the list of common names corresponding to the SID structures returned by ISecurityInformation2::LookupSids.
old-location: security\sid_info.htm
old-project: SecAuthZ
ms.assetid: 6a69e5b9-ab6a-4bbb-9f1a-5882d4c8038c
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: "*PSID_INFO, PSID_INFO, PSID_INFO structure pointer [Security], SID_INFO, SID_INFO structure [Security], _SID_INFO, _win32_sid_info_str, aclui/PSID_INFO, aclui/SID_INFO, security.sid_info"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: aclui.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SID_INFO, *PSID_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Aclui.h
api_name:
-	SID_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _SID_INFO structure


## -description


The <b>SID_INFO</b> structure contains the list of common names corresponding to the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structures returned by 
<a href="https://msdn.microsoft.com/9a4056c6-6a21-4051-b4a6-c77351fce983">ISecurityInformation2::LookupSids</a>. It is a member of the 
<a href="https://msdn.microsoft.com/e9be644c-ec56-4a49-9aa8-6b3f62d6cf0d">SID_INFO_LIST</a> structure.


## -struct-fields




### -field pSid

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure that identifies one of the SIDs passed into 
<a href="https://msdn.microsoft.com/9a4056c6-6a21-4051-b4a6-c77351fce983">ISecurityInformation2::LookupSids</a>.


### -field pwzCommonName

A pointer to a string containing the common name corresponding to the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure specified in <b>pSid</b>.


### -field pwzClass

A pointer to a string describing the <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure as either a user or a group. The possible values of this string are as follows:

<p class="indent">"Computer"

<p class="indent">"Group"

<p class="indent">"User"


### -field pwzUPN

A pointer to the user principal name (UPN) corresponding to the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure specified in <b>pSid</b>. If a UPN has not been designated for the <b>SID</b> structure, the value of this parameter is <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/9a4056c6-6a21-4051-b4a6-c77351fce983">ISecurityInformation2::LookupSids</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>
 

 

