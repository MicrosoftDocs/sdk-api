---
UID: NS:sessdirpublictypes.__MIDL___MIDL_itf_sessdirpublictypes_0000_0000_0001
title: "__MIDL___MIDL_itf_sessdirpublictypes_0000_0000_0001"
author: windows-sdk-content
description: Contains information about the display of a Remote Desktop Connection (RDC) client.
old-location: termserv\client_display.htm
old-project: TermServ
ms.assetid: 6436c049-d710-4208-882a-0c7e83b4a079
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: "*PCLIENT_DISPLAY, CLIENT_DISPLAY, CLIENT_DISPLAY structure [Remote Desktop Services], PCLIENT_DISPLAY, PCLIENT_DISPLAY structure pointer [Remote Desktop Services], __MIDL___MIDL_itf_sessdirpublictypes_0000_0000_0001, sessdirpublictypes/CLIENT_DISPLAY, sessdirpublictypes/PCLIENT_DISPLAY, termserv.client_display"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: sessdirpublictypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SessDirPublicTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CLIENT_DISPLAY, *PCLIENT_DISPLAY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SessDirPublicTypes.h
api_name:
 - CLIENT_DISPLAY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# __MIDL___MIDL_itf_sessdirpublictypes_0000_0000_0001 structure


## -description


Contains information about the display of a Remote Desktop Connection (RDC) client.


## -struct-fields




### -field HorizontalResolution

The horizontal dimension, in pixels, of the client's display.


### -field VerticalResolution

The vertical dimension, in pixels, of the client's display.


### -field ColorDepth

The color depth of the client's display. For possible values, see the <b>ColorDepth</b> member of the <a href="https://msdn.microsoft.com/0d5e0a9d-23b0-4302-ade3-eb9fbd7f787d">WTS_CLIENT_DISPLAY</a> structure.

