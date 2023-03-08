---
UID: NE:netcon.tagSHARINGCONNECTIONTYPE
title: SHARINGCONNECTIONTYPE (netcon.h)
description: The values of the SHARINGCONNECTIONTYPE type enumerate the possible types of shared connections.
helpviewer_keywords: ["*LPSHARINGCONNECTIONTYPE","ICSSHARINGTYPE_PRIVATE","ICSSHARINGTYPE_PUBLIC","LPSHARINGCONNECTIONTYPE","LPSHARINGCONNECTIONTYPE enumeration pointer [ICS/ICF]","SHARINGCONNECTIONTYPE","SHARINGCONNECTIONTYPE enumeration [ICS/ICF]","_ics_sharingconnectiontype","ics.sharingconnectiontype","netcon/ICSSHARINGTYPE_PRIVATE","netcon/ICSSHARINGTYPE_PUBLIC","netcon/LPSHARINGCONNECTIONTYPE","netcon/SHARINGCONNECTIONTYPE"]
old-location: ics\sharingconnectiontype.htm
tech.root: ics
ms.assetid: 97409190-55b3-412f-b654-e5b27928a4c3
ms.date: 12/05/2018
ms.keywords: '*LPSHARINGCONNECTIONTYPE, ICSSHARINGTYPE_PRIVATE, ICSSHARINGTYPE_PUBLIC, LPSHARINGCONNECTIONTYPE, LPSHARINGCONNECTIONTYPE enumeration pointer [ICS/ICF], SHARINGCONNECTIONTYPE, SHARINGCONNECTIONTYPE enumeration [ICS/ICF], _ics_sharingconnectiontype, ics.sharingconnectiontype, netcon/ICSSHARINGTYPE_PRIVATE, netcon/ICSSHARINGTYPE_PUBLIC, netcon/LPSHARINGCONNECTIONTYPE, netcon/SHARINGCONNECTIONTYPE'
req.header: netcon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: SHARINGCONNECTIONTYPE, *LPSHARINGCONNECTIONTYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSHARINGCONNECTIONTYPE
 - netcon/tagSHARINGCONNECTIONTYPE
 - LPSHARINGCONNECTIONTYPE
 - netcon/LPSHARINGCONNECTIONTYPE
 - SHARINGCONNECTIONTYPE
 - netcon/SHARINGCONNECTIONTYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - NetCon.h
api_name:
 - SHARINGCONNECTIONTYPE
---

# SHARINGCONNECTIONTYPE enumeration


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The values of the 
<b>SHARINGCONNECTIONTYPE</b> type enumerate the possible types of shared connections.

## -enum-fields

### -field ICSSHARINGTYPE_PUBLIC:0

The connection is public.

### -field ICSSHARINGTYPE_PRIVATE

The connection is private.

## -see-also

<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-get_sharingenabled">INetSharingConfiguration::get_SharingEnabled</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-enumeration-types">Internet Connection Sharing and Internet Connection Firewall Enumeration Types</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>
