---
UID: NE:peerdist._PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS
title: PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS (peerdist.h)
description: The PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS enumeration defines the possible client information values.
helpviewer_keywords: ["*PPEERDIST_CLIENT_INFO_BY_HANDLE_CLASS","MaximumPeerDistClientInfoByHandlesClass","PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS","PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS enumeration [Peer Networking]","PPEERDIST_CLIENT_INFO_BY_HANDLE_CLASS","PPEERDIST_CLIENT_INFO_BY_HANDLE_CLASS enumeration pointer [Peer Networking]","PeerDistClientBasicInfo","p2p.peerdist_client_info_by_handle_class","peerdist/MaximumPeerDistClientInfoByHandlesClass","peerdist/PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS","peerdist/PPEERDIST_CLIENT_INFO_BY_HANDLE_CLASS","peerdist/PeerDistClientBasicInfo"]
old-location: p2p\peerdist_client_info_by_handle_class.htm
tech.root: p2p
ms.assetid: 28391dc5-ec89-44d9-acac-b7ff3868e542
ms.date: 12/05/2018
ms.keywords: '*PPEERDIST_CLIENT_INFO_BY_HANDLE_CLASS, MaximumPeerDistClientInfoByHandlesClass, PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS, PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS enumeration [Peer Networking], PPEERDIST_CLIENT_INFO_BY_HANDLE_CLASS, PPEERDIST_CLIENT_INFO_BY_HANDLE_CLASS enumeration pointer [Peer Networking], PeerDistClientBasicInfo, p2p.peerdist_client_info_by_handle_class, peerdist/MaximumPeerDistClientInfoByHandlesClass, peerdist/PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS, peerdist/PPEERDIST_CLIENT_INFO_BY_HANDLE_CLASS, peerdist/PeerDistClientBasicInfo'
req.header: peerdist.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS, *PPEERDIST_CLIENT_INFO_BY_HANDLE_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS
 - peerdist/_PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS
 - PPEERDIST_CLIENT_INFO_BY_HANDLE_CLASS
 - peerdist/PPEERDIST_CLIENT_INFO_BY_HANDLE_CLASS
 - PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS
 - peerdist/PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - peerdist.h
api_name:
 - PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS
---

# PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS enumeration


## -description

The <b>PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS</b> enumeration defines the possible client information values.

## -enum-fields

### -field PeerDistClientBasicInfo:0

 Indicates the information to retrieve is a <a href="/windows/desktop/api/peerdist/ns-peerdist-peerdist_client_basic_info">PEERDIST_CLIENT_BASIC_INFO</a> structure.

### -field MaximumPeerDistClientInfoByHandlesClass

The maximum value for the enumeration that is used for error checking.  This value should not be sent to the <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientgetinformationbyhandle">PeerDistClientGetInformationByHandle</a> function.

## -remarks

A value from this enumeration is passed to the<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientgetinformationbyhandle">PeerDistClientGetInformationByHandle</a> function as the <i>PeerDistClientInfoClass</i> parameter.

## -see-also

<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientgetinformationbyhandle">PeerDistClientGetInformationByHandle</a>
