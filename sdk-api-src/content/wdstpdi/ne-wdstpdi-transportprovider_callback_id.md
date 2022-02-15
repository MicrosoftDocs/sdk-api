---
UID: NE:wdstpdi._TRANSPORTPROVIDER_CALLBACK_ID
title: TRANSPORTPROVIDER_CALLBACK_ID (wdstpdi.h)
description: This structure is used by the WdsTransportServerRegisterCallback function.
helpviewer_keywords: ["*PTRANSPORTPROVIDER_CALLBACK_ID","TRANSPORTPROVIDER_CALLBACK_ID","TRANSPORTPROVIDER_CALLBACK_ID enumeration [Windows Deployment Services]","TRANSPORTPROVIDER_CALLBACK_ID","*PTRANSPORTPROVIDER_CALLBACK_ID","TRANSPORTPROVIDER_CALLBACK_ID","*PTRANSPORTPROVIDER_CALLBACK_ID enumeration [Windows Deployment Services]","WDS_TRANSPORTPROVIDER_CLOSE_CONTENT","WDS_TRANSPORTPROVIDER_CLOSE_INSTANCE","WDS_TRANSPORTPROVIDER_COMPARE_CONTENT","WDS_TRANSPORTPROVIDER_CREATE_INSTANCE","WDS_TRANSPORTPROVIDER_DUMP_STATE","WDS_TRANSPORTPROVIDER_GET_CONTENT_METADATA","WDS_TRANSPORTPROVIDER_GET_CONTENT_SIZE","WDS_TRANSPORTPROVIDER_MAX_CALLBACKS","WDS_TRANSPORTPROVIDER_OPEN_CONTENT","WDS_TRANSPORTPROVIDER_READ_CONTENT","WDS_TRANSPORTPROVIDER_REFRESH_SETTINGS","WDS_TRANSPORTPROVIDER_SHUTDOWN","WDS_TRANSPORTPROVIDER_USER_ACCESS_CHECK","wds.transportprovider_callback_id","wdstpdi/ WDS_TRANSPORTPROVIDER_GET_CONTENT_METADATA","wdstpdi/ WDS_TRANSPORTPROVIDER_MAX_CALLBACKS","wdstpdi/TRANSPORTPROVIDER_CALLBACK_ID","wdstpdi/WDS_TRANSPORTPROVIDER_CLOSE_CONTENT","wdstpdi/WDS_TRANSPORTPROVIDER_CLOSE_INSTANCE","wdstpdi/WDS_TRANSPORTPROVIDER_COMPARE_CONTENT","wdstpdi/WDS_TRANSPORTPROVIDER_CREATE_INSTANCE","wdstpdi/WDS_TRANSPORTPROVIDER_DUMP_STATE","wdstpdi/WDS_TRANSPORTPROVIDER_GET_CONTENT_SIZE","wdstpdi/WDS_TRANSPORTPROVIDER_OPEN_CONTENT","wdstpdi/WDS_TRANSPORTPROVIDER_READ_CONTENT","wdstpdi/WDS_TRANSPORTPROVIDER_REFRESH_SETTINGS","wdstpdi/WDS_TRANSPORTPROVIDER_SHUTDOWN","wdstpdi/WDS_TRANSPORTPROVIDER_USER_ACCESS_CHECK"]
old-location: wds\transportprovider_callback_id.htm
tech.root: wds
ms.assetid: 5e91f39b-4876-4523-817f-91467469344f
ms.date: 12/05/2018
ms.keywords: '*PTRANSPORTPROVIDER_CALLBACK_ID, TRANSPORTPROVIDER_CALLBACK_ID, TRANSPORTPROVIDER_CALLBACK_ID enumeration [Windows Deployment Services], TRANSPORTPROVIDER_CALLBACK_ID,*PTRANSPORTPROVIDER_CALLBACK_ID, TRANSPORTPROVIDER_CALLBACK_ID,*PTRANSPORTPROVIDER_CALLBACK_ID enumeration [Windows Deployment Services], WDS_TRANSPORTPROVIDER_CLOSE_CONTENT, WDS_TRANSPORTPROVIDER_CLOSE_INSTANCE, WDS_TRANSPORTPROVIDER_COMPARE_CONTENT, WDS_TRANSPORTPROVIDER_CREATE_INSTANCE, WDS_TRANSPORTPROVIDER_DUMP_STATE, WDS_TRANSPORTPROVIDER_GET_CONTENT_METADATA, WDS_TRANSPORTPROVIDER_GET_CONTENT_SIZE, WDS_TRANSPORTPROVIDER_MAX_CALLBACKS, WDS_TRANSPORTPROVIDER_OPEN_CONTENT, WDS_TRANSPORTPROVIDER_READ_CONTENT, WDS_TRANSPORTPROVIDER_REFRESH_SETTINGS, WDS_TRANSPORTPROVIDER_SHUTDOWN, WDS_TRANSPORTPROVIDER_USER_ACCESS_CHECK, wds.transportprovider_callback_id, wdstpdi/ WDS_TRANSPORTPROVIDER_GET_CONTENT_METADATA, wdstpdi/ WDS_TRANSPORTPROVIDER_MAX_CALLBACKS, wdstpdi/TRANSPORTPROVIDER_CALLBACK_ID, wdstpdi/WDS_TRANSPORTPROVIDER_CLOSE_CONTENT, wdstpdi/WDS_TRANSPORTPROVIDER_CLOSE_INSTANCE, wdstpdi/WDS_TRANSPORTPROVIDER_COMPARE_CONTENT, wdstpdi/WDS_TRANSPORTPROVIDER_CREATE_INSTANCE, wdstpdi/WDS_TRANSPORTPROVIDER_DUMP_STATE, wdstpdi/WDS_TRANSPORTPROVIDER_GET_CONTENT_SIZE, wdstpdi/WDS_TRANSPORTPROVIDER_OPEN_CONTENT, wdstpdi/WDS_TRANSPORTPROVIDER_READ_CONTENT, wdstpdi/WDS_TRANSPORTPROVIDER_REFRESH_SETTINGS, wdstpdi/WDS_TRANSPORTPROVIDER_SHUTDOWN, wdstpdi/WDS_TRANSPORTPROVIDER_USER_ACCESS_CHECK'
req.header: wdstpdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP2 [desktop apps only]
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
req.typenames: TRANSPORTPROVIDER_CALLBACK_ID, *PTRANSPORTPROVIDER_CALLBACK_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TRANSPORTPROVIDER_CALLBACK_ID
 - wdstpdi/_TRANSPORTPROVIDER_CALLBACK_ID
 - PTRANSPORTPROVIDER_CALLBACK_ID
 - wdstpdi/PTRANSPORTPROVIDER_CALLBACK_ID
 - TRANSPORTPROVIDER_CALLBACK_ID
 - wdstpdi/TRANSPORTPROVIDER_CALLBACK_ID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wdstpdi.h
api_name:
 - TRANSPORTPROVIDER_CALLBACK_ID, *PTRANSPORTPROVIDER_CALLBACK_ID
---

# TRANSPORTPROVIDER_CALLBACK_ID enumeration


## -description

This structure is used by the <a href="/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportserverregistercallback">WdsTransportServerRegisterCallback</a> function.

## -enum-fields

### -field WDS_TRANSPORTPROVIDER_CREATE_INSTANCE:0

Identifies the <a href="/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercreateinstance">WdsTransportProviderCreateInstance</a> callback.

### -field WDS_TRANSPORTPROVIDER_COMPARE_CONTENT

Identifies the <a href="/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercomparecontent">WdsTransportProviderCompareContent</a> callback.

### -field WDS_TRANSPORTPROVIDER_OPEN_CONTENT

Identifies the <a href="/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideropencontent">WdsTransportProviderOpenContent</a> callback.

### -field WDS_TRANSPORTPROVIDER_USER_ACCESS_CHECK

Identifies the <a href="/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideruseraccesscheck">WdsTransportProviderUserAccessCheck</a> callback.

### -field WDS_TRANSPORTPROVIDER_GET_CONTENT_SIZE

Identifies the <a href="/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentsize">WdsTransportProviderGetContentSize</a> callback.

### -field WDS_TRANSPORTPROVIDER_READ_CONTENT

Identifies the <a href="/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderreadcontent">WdsTransportProviderReadContent</a> callback.

### -field WDS_TRANSPORTPROVIDER_CLOSE_CONTENT

Identifies the <a href="/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderclosecontent">WdsTransportProviderCloseContent</a> callback.

### -field WDS_TRANSPORTPROVIDER_CLOSE_INSTANCE

Identifies the <a href="/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercloseinstance">WdsTransportProviderCloseInstance</a> callback.

### -field WDS_TRANSPORTPROVIDER_SHUTDOWN

Identifies the <a href="/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidershutdown">WdsTransportProviderShutdown</a> callback.

### -field WDS_TRANSPORTPROVIDER_DUMP_STATE

Identifies the <a href="/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderdumpstate">WdsTransportProviderDumpState</a> callback.

### -field WDS_TRANSPORTPROVIDER_REFRESH_SETTINGS

Identifies the <a href="/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderrefreshsettings">WdsTransportProviderRefreshSettings</a> callback.

### -field WDS_TRANSPORTPROVIDER_GET_CONTENT_METADATA

Identifies the <a href="/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentmetadata">WdsTransportProviderGetContentMetadata</a> callback.

### -field WDS_TRANSPORTPROVIDER_MAX_CALLBACKS

Used for validation checking.
