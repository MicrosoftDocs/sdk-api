---
UID: NE:wdstci._TRANSPORTCLIENT_CALLBACK_ID
title: TRANSPORTCLIENT_CALLBACK_ID (wdstci.h)
description: This enumeration is received by the WdsTransportClientRegisterCallback function.
helpviewer_keywords: ["*PTRANSPORTCLIENT_CALLBACK_ID","TRANSPORTCLIENT_CALLBACK_ID","TRANSPORTCLIENT_CALLBACK_ID enumeration [Windows Deployment Services]","TRANSPORTCLIENT_CALLBACK_ID","*PTRANSPORTCLIENT_CALLBACK_ID","TRANSPORTCLIENT_CALLBACK_ID","*PTRANSPORTCLIENT_CALLBACK_ID enumeration [Windows Deployment Services]","WDS_TRANSPORTCLIENT_MAX_CALLBACKS","WDS_TRANSPORTCLIENT_RECEIVE_CONTENTS","WDS_TRANSPORTCLIENT_RECEIVE_METADATA","WDS_TRANSPORTCLIENT_SESSION_COMPLETE","WDS_TRANSPORTCLIENT_SESSION_START","WDS_TRANSPORTCLIENT_SESSION_STARTEX","wds.transportclient_callback_id","wdstci/ WDS_TRANSPORTCLIENT_SESSION_STARTEX","wdstci/TRANSPORTCLIENT_CALLBACK_ID","wdstci/WDS_TRANSPORTCLIENT_MAX_CALLBACKS","wdstci/WDS_TRANSPORTCLIENT_RECEIVE_CONTENTS","wdstci/WDS_TRANSPORTCLIENT_RECEIVE_METADATA","wdstci/WDS_TRANSPORTCLIENT_SESSION_COMPLETE","wdstci/WDS_TRANSPORTCLIENT_SESSION_START"]
old-location: wds\transportclient_callback_id.htm
tech.root: wds
ms.assetid: 6dd5e1ed-a9f8-4c6b-8bbb-8e3e6551d980
ms.date: 12/05/2018
ms.keywords: '*PTRANSPORTCLIENT_CALLBACK_ID, TRANSPORTCLIENT_CALLBACK_ID, TRANSPORTCLIENT_CALLBACK_ID enumeration [Windows Deployment Services], TRANSPORTCLIENT_CALLBACK_ID,*PTRANSPORTCLIENT_CALLBACK_ID, TRANSPORTCLIENT_CALLBACK_ID,*PTRANSPORTCLIENT_CALLBACK_ID enumeration [Windows Deployment Services], WDS_TRANSPORTCLIENT_MAX_CALLBACKS, WDS_TRANSPORTCLIENT_RECEIVE_CONTENTS, WDS_TRANSPORTCLIENT_RECEIVE_METADATA, WDS_TRANSPORTCLIENT_SESSION_COMPLETE, WDS_TRANSPORTCLIENT_SESSION_START, WDS_TRANSPORTCLIENT_SESSION_STARTEX, wds.transportclient_callback_id, wdstci/ WDS_TRANSPORTCLIENT_SESSION_STARTEX, wdstci/TRANSPORTCLIENT_CALLBACK_ID, wdstci/WDS_TRANSPORTCLIENT_MAX_CALLBACKS, wdstci/WDS_TRANSPORTCLIENT_RECEIVE_CONTENTS, wdstci/WDS_TRANSPORTCLIENT_RECEIVE_METADATA, wdstci/WDS_TRANSPORTCLIENT_SESSION_COMPLETE, wdstci/WDS_TRANSPORTCLIENT_SESSION_START'
req.header: wdstci.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: TRANSPORTCLIENT_CALLBACK_ID, *PTRANSPORTCLIENT_CALLBACK_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TRANSPORTCLIENT_CALLBACK_ID
 - wdstci/_TRANSPORTCLIENT_CALLBACK_ID
 - PTRANSPORTCLIENT_CALLBACK_ID
 - wdstci/PTRANSPORTCLIENT_CALLBACK_ID
 - TRANSPORTCLIENT_CALLBACK_ID
 - wdstci/TRANSPORTCLIENT_CALLBACK_ID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wdstci.h
api_name:
 - TRANSPORTCLIENT_CALLBACK_ID,*PTRANSPORTCLIENT_CALLBACK_ID
---

# TRANSPORTCLIENT_CALLBACK_ID enumeration


## -description

This enumeration is received  by the <a href="/windows/desktop/api/wdstci/nf-wdstci-wdstransportclientregistercallback">WdsTransportClientRegisterCallback</a> function.

## -enum-fields

### -field WDS_TRANSPORTCLIENT_SESSION_START:0

Identifies the <a href="/windows/desktop/api/wdstci/nc-wdstci-pfn_wdstransportclientsessionstart">PFN_WdsTransportClientSessionStart</a> callback.

### -field WDS_TRANSPORTCLIENT_RECEIVE_CONTENTS

Identifies the <a href="/windows/desktop/api/wdstci/nc-wdstci-pfn_wdstransportclientreceivecontents">PFN_WdsTransportClientReceiveContents</a> callback.

### -field WDS_TRANSPORTCLIENT_SESSION_COMPLETE

Identifies the <a href="/windows/desktop/api/wdstci/nc-wdstci-pfn_wdstransportclientsessioncomplete">PFN_WdsTransportClientSessionComplete</a> callback.

### -field WDS_TRANSPORTCLIENT_RECEIVE_METADATA

Identifies the <a href="/windows/desktop/api/wdstci/nc-wdstci-pfn_wdstransportclientreceivemetadata">PFN_WdsTransportClientReceiveMetadata</a> callback.

### -field WDS_TRANSPORTCLIENT_SESSION_STARTEX

Identifies the <a href="/windows/desktop/api/wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex">PFN_WdsTransportClientSessionStartEx</a> callback.

### -field WDS_TRANSPORTCLIENT_SESSION_NEGOTIATE

### -field WDS_TRANSPORTCLIENT_MAX_CALLBACKS

Used for validation checking.
