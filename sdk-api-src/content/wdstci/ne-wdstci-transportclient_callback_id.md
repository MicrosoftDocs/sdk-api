---
UID: NE:wdstci._TRANSPORTCLIENT_CALLBACK_ID
title: TRANSPORTCLIENT_CALLBACK_ID (wdstci.h)
author: windows-sdk-content
description: This enumeration is received by the WdsTransportClientRegisterCallback function.
old-location: wds\transportclient_callback_id.htm
tech.root: wds
ms.assetid: 6dd5e1ed-a9f8-4c6b-8bbb-8e3e6551d980
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PTRANSPORTCLIENT_CALLBACK_ID, TRANSPORTCLIENT_CALLBACK_ID, TRANSPORTCLIENT_CALLBACK_ID enumeration [Windows Deployment Services], TRANSPORTCLIENT_CALLBACK_ID,*PTRANSPORTCLIENT_CALLBACK_ID, TRANSPORTCLIENT_CALLBACK_ID,*PTRANSPORTCLIENT_CALLBACK_ID enumeration [Windows Deployment Services], WDS_TRANSPORTCLIENT_MAX_CALLBACKS, WDS_TRANSPORTCLIENT_RECEIVE_CONTENTS, WDS_TRANSPORTCLIENT_RECEIVE_METADATA, WDS_TRANSPORTCLIENT_SESSION_COMPLETE, WDS_TRANSPORTCLIENT_SESSION_START, WDS_TRANSPORTCLIENT_SESSION_STARTEX, wds.transportclient_callback_id, wdstci/ WDS_TRANSPORTCLIENT_SESSION_STARTEX, wdstci/TRANSPORTCLIENT_CALLBACK_ID, wdstci/WDS_TRANSPORTCLIENT_MAX_CALLBACKS, wdstci/WDS_TRANSPORTCLIENT_RECEIVE_CONTENTS, wdstci/WDS_TRANSPORTCLIENT_RECEIVE_METADATA, wdstci/WDS_TRANSPORTCLIENT_SESSION_COMPLETE, wdstci/WDS_TRANSPORTCLIENT_SESSION_START"
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wdstci.h
api_name:
 - TRANSPORTCLIENT_CALLBACK_ID,*PTRANSPORTCLIENT_CALLBACK_ID
product: Windows
targetos: Windows
req.typenames: TRANSPORTCLIENT_CALLBACK_ID, *PTRANSPORTCLIENT_CALLBACK_ID
req.redist: 
ms.custom: 19H1
---

# TRANSPORTCLIENT_CALLBACK_ID enumeration


## -description


This enumeration is received  by the <a href="https://msdn.microsoft.com/e3c809c4-5681-4979-8633-bb8d3dbde35b">WdsTransportClientRegisterCallback</a> function.


## -enum-fields




### -field WDS_TRANSPORTCLIENT_SESSION_START

Identifies the <a href="https://msdn.microsoft.com/47a053e3-f457-4d0a-80a8-1b93d5e8688f">PFN_WdsTransportClientSessionStart</a> callback.


### -field WDS_TRANSPORTCLIENT_RECEIVE_CONTENTS

Identifies the <a href="https://msdn.microsoft.com/3a1cd9bb-c0da-4d66-9338-1f284fc15499">PFN_WdsTransportClientReceiveContents</a> callback.


### -field WDS_TRANSPORTCLIENT_SESSION_COMPLETE

Identifies the <a href="https://msdn.microsoft.com/1c7b8137-bf74-486c-a90e-6becfec5ddc8">PFN_WdsTransportClientSessionComplete</a> callback.


### -field WDS_TRANSPORTCLIENT_RECEIVE_METADATA

Identifies the <a href="https://msdn.microsoft.com/9acde77b-5360-4c55-b11d-bf85e5c8d00e">PFN_WdsTransportClientReceiveMetadata</a> callback.


### -field WDS_TRANSPORTCLIENT_SESSION_STARTEX

Identifies the <a href="https://msdn.microsoft.com/36970f1b-9dbf-421f-a078-3da3bbb050e8">PFN_WdsTransportClientSessionStartEx</a> callback.


### -field WDS_TRANSPORTCLIENT_SESSION_NEGOTIATE


### -field WDS_TRANSPORTCLIENT_MAX_CALLBACKS

Used for validation checking.

