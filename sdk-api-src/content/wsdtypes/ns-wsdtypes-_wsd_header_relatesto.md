---
UID: NS:wsdtypes._WSD_HEADER_RELATESTO
title: "_WSD_HEADER_RELATESTO"
author: windows-sdk-content
description: Represents a RelatesTo SOAP envelope header block, as specified by the WS-Addressing specification.
old-location: ncd\wsd_header_relatesto.htm
tech.root: WsdApi
ms.assetid: 6085620e-2e3d-4e77-90cd-7cb9fd2c197e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WSD_HEADER_RELATESTO, WSD_HEADER_RELATESTO structure, _WSD_HEADER_RELATESTO, ncd.wsd_header_relatesto, ncd.wsd_header_relayesto, wsdtypes/WSD_HEADER_RELATESTO
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wsdtypes.h
req.include-header: Wsdapi.h
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
 - WsdTypes.h
api_name:
 - WSD_HEADER_RELATESTO
product: Windows
targetos: Windows
req.typenames: WSD_HEADER_RELATESTO
req.redist: 
---

# _WSD_HEADER_RELATESTO structure


## -description


Represents a RelatesTo SOAP envelope header block, as specified by the WS-Addressing specification.


## -struct-fields




### -field RelationshipType

Reference to a <a href="https://msdn.microsoft.com/9dce71d2-700c-4f86-9308-dee6a69010bb">WSDXML_NAME</a> structure that contains the relationship type as a qualified name.


### -field MessageID

The identifier of the related message.

