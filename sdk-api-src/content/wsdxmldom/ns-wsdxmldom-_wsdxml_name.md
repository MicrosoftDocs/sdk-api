---
UID: NS:wsdxmldom._WSDXML_NAME
title: "_WSDXML_NAME"
author: windows-sdk-content
description: Specifies an XML qualified name.
old-location: ncd\wsdxml_name_struct.htm
tech.root: WsdApi
ms.assetid: 9dce71d2-700c-4f86-9308-dee6a69010bb
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: WSDXML_NAME, WSDXML_NAME structure, _WSDXML_NAME, ncd.wsdxml_name_struct, wsdxmldom/WSDXML_NAME
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wsdxmldom.h
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
 - WsdXmldom.h
api_name:
 - WSDXML_NAME
product: Windows
targetos: Windows
req.typenames: WSDXML_NAME
req.redist: 
---

# _WSDXML_NAME structure


## -description


Specifies an XML qualified name.


## -struct-fields




### -field Space

Reference to a <a href="https://msdn.microsoft.com/dcf27f38-e628-4b0c-859c-ad12d3ed0924">WSDXML_NAMESPACE</a> structure that specifies the namespace of the qualified name.


### -field LocalName

The local name of the qualified name.


## -remarks



<b>WSDXML_NAME</b> represents a single name within a namespace. The relationship between the name and namespace is circular, in that the <b>Space</b> pointer of the name points to the namespace the name belongs to, and the <b>Names</b> array of the namespace will have an entry for the name.



