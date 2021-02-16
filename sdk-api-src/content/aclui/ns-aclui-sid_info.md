---
UID: NS:aclui._SID_INFO
title: SID_INFO (aclui.h)
description: Contains the list of common names corresponding to the SID structures returned by ISecurityInformation2::LookupSids.
helpviewer_keywords: ["*PSID_INFO","PSID_INFO","PSID_INFO structure pointer [Security]","SID_INFO","SID_INFO structure [Security]","_win32_sid_info_str","aclui/PSID_INFO","aclui/SID_INFO","security.sid_info"]
old-location: security\sid_info.htm
tech.root: security
ms.assetid: 6a69e5b9-ab6a-4bbb-9f1a-5882d4c8038c
ms.date: 12/05/2018
ms.keywords: '*PSID_INFO, PSID_INFO, PSID_INFO structure pointer [Security], SID_INFO, SID_INFO structure [Security], _win32_sid_info_str, aclui/PSID_INFO, aclui/SID_INFO, security.sid_info'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SID_INFO, *PSID_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SID_INFO
 - aclui/_SID_INFO
 - PSID_INFO
 - aclui/PSID_INFO
 - SID_INFO
 - aclui/SID_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Aclui.h
api_name:
 - SID_INFO
---

# SID_INFO structure


## -description

The <b>SID_INFO</b> structure contains the list of common names corresponding to the 
<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structures returned by 
<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation2-lookupsids">ISecurityInformation2::LookupSids</a>. It is a member of the 
<a href="/windows/desktop/api/aclui/ns-aclui-sid_info_list">SID_INFO_LIST</a> structure.

## -struct-fields

### -field pSid

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure that identifies one of the SIDs passed into 
<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation2-lookupsids">ISecurityInformation2::LookupSids</a>.

### -field pwzCommonName

A pointer to a string containing the common name corresponding to the 
<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure specified in <b>pSid</b>.

### -field pwzClass

A pointer to a string describing the <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure as either a user or a group. The possible values of this string are as follows:

<p class="indent">"Computer"

<p class="indent">"Group"

<p class="indent">"User"

### -field pwzUPN

A pointer to the user principal name (UPN) corresponding to the 
<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure specified in <b>pSid</b>. If a UPN has not been designated for the <b>SID</b> structure, the value of this parameter is <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation2-lookupsids">ISecurityInformation2::LookupSids</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>