---
UID: NS:aclui._SID_INFO_LIST
title: SID_INFO_LIST (aclui.h)
description: Contains a list of SID_INFO structures.
helpviewer_keywords: ["*PSID_INFO_LIST","PSID_INFO_LIST","PSID_INFO_LIST structure pointer [Security]","SID_INFO_LIST","SID_INFO_LIST structure [Security]","_win32_sid_info_list_str","aclui/PSID_INFO_LIST","aclui/SID_INFO_LIST","security.sid_info_list"]
old-location: security\sid_info_list.htm
tech.root: security
ms.assetid: e9be644c-ec56-4a49-9aa8-6b3f62d6cf0d
ms.date: 12/05/2018
ms.keywords: '*PSID_INFO_LIST, PSID_INFO_LIST, PSID_INFO_LIST structure pointer [Security], SID_INFO_LIST, SID_INFO_LIST structure [Security], _win32_sid_info_list_str, aclui/PSID_INFO_LIST, aclui/SID_INFO_LIST, security.sid_info_list'
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
req.typenames: SID_INFO_LIST, *PSID_INFO_LIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SID_INFO_LIST
 - aclui/_SID_INFO_LIST
 - PSID_INFO_LIST
 - aclui/PSID_INFO_LIST
 - SID_INFO_LIST
 - aclui/SID_INFO_LIST
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
 - SID_INFO_LIST
---

# SID_INFO_LIST structure


## -description

The <b>SID_INFO_LIST</b> structure contains a list of 
<a href="/windows/desktop/api/aclui/ns-aclui-sid_info">SID_INFO</a> structures.

## -struct-fields

### -field cItems

The number of 
<a href="/windows/desktop/api/aclui/ns-aclui-sid_info">SID_INFO</a> structures contained in the <b>aSidInfo</b> member.

### -field aSidInfo

A pointer to a list of <a href="/windows/desktop/api/aclui/ns-aclui-sid_info">SID_INFO</a> structures that is returned by the 
<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation2-lookupsids">ISecurityInformation2::LookupSids</a> method.

## -see-also

<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation2-lookupsids">ISecurityInformation2::LookupSids</a>



<a href="/windows/desktop/api/aclui/ns-aclui-sid_info">SID_INFO</a>