---
UID: NE:wdstpdi._TRANSPORTPROVIDER_CALLBACK_ID
title: "_TRANSPORTPROVIDER_CALLBACK_ID"
author: windows-driver-content
description: This structure is used by the WdsTransportServerRegisterCallback function.
old-location: wds\transportprovider_callback_id.htm
old-project: Wds
ms.assetid: 5e91f39b-4876-4523-817f-91467469344f
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: "*PTRANSPORTPROVIDER_CALLBACK_ID, TRANSPORTPROVIDER_CALLBACK_ID, TRANSPORTPROVIDER_CALLBACK_ID enumeration [Windows Deployment Services], TRANSPORTPROVIDER_CALLBACK_ID,*PTRANSPORTPROVIDER_CALLBACK_ID, TRANSPORTPROVIDER_CALLBACK_ID,*PTRANSPORTPROVIDER_CALLBACK_ID enumeration [Windows Deployment Services], WDS_TRANSPORTPROVIDER_CLOSE_CONTENT, WDS_TRANSPORTPROVIDER_CLOSE_INSTANCE, WDS_TRANSPORTPROVIDER_COMPARE_CONTENT, WDS_TRANSPORTPROVIDER_CREATE_INSTANCE, WDS_TRANSPORTPROVIDER_DUMP_STATE, WDS_TRANSPORTPROVIDER_GET_CONTENT_METADATA, WDS_TRANSPORTPROVIDER_GET_CONTENT_SIZE, WDS_TRANSPORTPROVIDER_MAX_CALLBACKS, WDS_TRANSPORTPROVIDER_OPEN_CONTENT, WDS_TRANSPORTPROVIDER_READ_CONTENT, WDS_TRANSPORTPROVIDER_REFRESH_SETTINGS, WDS_TRANSPORTPROVIDER_SHUTDOWN, WDS_TRANSPORTPROVIDER_USER_ACCESS_CHECK, _TRANSPORTPROVIDER_CALLBACK_ID, wds.transportprovider_callback_id, wdstpdi/ WDS_TRANSPORTPROVIDER_GET_CONTENT_METADATA, wdstpdi/ WDS_TRANSPORTPROVIDER_MAX_CALLBACKS, wdstpdi/TRANSPORTPROVIDER_CALLBACK_ID, wdstpdi/WDS_TRANSPORTPROVIDER_CLOSE_CONTENT, wdstpdi/WDS_TRANSPORTPROVIDER_CLOSE_INSTANCE, wdstpdi/WDS_TRANSPORTPROVIDER_COMPARE_CONTENT, wdstpdi/WDS_TRANSPORTPROVIDER_CREATE_INSTANCE, wdstpdi/WDS_TRANSPORTPROVIDER_DUMP_STATE, wdstpdi/WDS_TRANSPORTPROVIDER_GET_CONTENT_SIZE, wdstpdi/WDS_TRANSPORTPROVIDER_OPEN_CONTENT, wdstpdi/WDS_TRANSPORTPROVIDER_READ_CONTENT, wdstpdi/WDS_TRANSPORTPROVIDER_REFRESH_SETTINGS, wdstpdi/WDS_TRANSPORTPROVIDER_SHUTDOWN, wdstpdi/WDS_TRANSPORTPROVIDER_USER_ACCESS_CHECK"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: TRANSPORTPROVIDER_CALLBACK_ID, *PTRANSPORTPROVIDER_CALLBACK_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wdstpdi.h
api_name:
-	TRANSPORTPROVIDER_CALLBACK_ID, *PTRANSPORTPROVIDER_CALLBACK_ID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _TRANSPORTPROVIDER_CALLBACK_ID enumeration


## -description


This structure is used by the <a href="https://msdn.microsoft.com/565ceb6c-0e44-4c71-8b67-092cd33d088e">WdsTransportServerRegisterCallback</a> function.


## -enum-fields




### -field WDS_TRANSPORTPROVIDER_CREATE_INSTANCE

Identifies the <a href="https://msdn.microsoft.com/534ba680-e5d7-47e7-83ad-2b621feab99f">WdsTransportProviderCreateInstance</a> callback.


### -field WDS_TRANSPORTPROVIDER_COMPARE_CONTENT

Identifies the <a href="https://msdn.microsoft.com/206b85e2-e139-4f62-9107-ed78893a7ad2">WdsTransportProviderCompareContent</a> callback.


### -field WDS_TRANSPORTPROVIDER_OPEN_CONTENT

Identifies the <a href="https://msdn.microsoft.com/95bea971-9c97-4d66-871d-5ef7407b9659">WdsTransportProviderOpenContent</a> callback.


### -field WDS_TRANSPORTPROVIDER_USER_ACCESS_CHECK

Identifies the <a href="https://msdn.microsoft.com/3ce381d3-d6f6-4f64-a825-116c3cff4747">WdsTransportProviderUserAccessCheck</a> callback.


### -field WDS_TRANSPORTPROVIDER_GET_CONTENT_SIZE

Identifies the <a href="https://msdn.microsoft.com/2ab55723-b55a-454e-92f8-164a07c86028">WdsTransportProviderGetContentSize</a> callback.


### -field WDS_TRANSPORTPROVIDER_READ_CONTENT

Identifies the <a href="https://msdn.microsoft.com/2b208871-a623-469b-a5dc-40d0c8009c02">WdsTransportProviderReadContent</a> callback.


### -field WDS_TRANSPORTPROVIDER_CLOSE_CONTENT

Identifies the <a href="https://msdn.microsoft.com/358fdf14-b57b-4c07-b0a5-d8f49aa96c21">WdsTransportProviderCloseContent</a> callback.


### -field WDS_TRANSPORTPROVIDER_CLOSE_INSTANCE

Identifies the <a href="https://msdn.microsoft.com/3eb0a931-ca5d-4db4-9c40-9c52f98be429">WdsTransportProviderCloseInstance</a> callback.


### -field WDS_TRANSPORTPROVIDER_SHUTDOWN

Identifies the <a href="https://msdn.microsoft.com/89f563e1-8dbd-4660-8cec-506f708ae310">WdsTransportProviderShutdown</a> callback.


### -field WDS_TRANSPORTPROVIDER_DUMP_STATE

Identifies the <a href="https://msdn.microsoft.com/e7a7d866-2954-46fb-8356-dbd7761efcf3">WdsTransportProviderDumpState</a> callback.


### -field WDS_TRANSPORTPROVIDER_REFRESH_SETTINGS

Identifies the <a href="https://msdn.microsoft.com/b5fc2340-6820-4b11-b96b-dcf3186f0786">WdsTransportProviderRefreshSettings</a> callback.


### -field WDS_TRANSPORTPROVIDER_GET_CONTENT_METADATA

Identifies the <a href="https://msdn.microsoft.com/ed243373-b5ff-418d-811c-544589ea11ac">WdsTransportProviderGetContentMetadata</a> callback.


### -field WDS_TRANSPORTPROVIDER_MAX_CALLBACKS

Used for validation checking.

