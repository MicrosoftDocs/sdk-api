---
UID: NE:objidlbase.tagEXTCONN
title: tagEXTCONN
author: windows-sdk-content
description: Specifies the type of external connection existing on an embedded object.
old-location: com\extconn.htm
old-project: com
ms.assetid: 95c7de47-9f81-4316-99b8-0f5f0aa54d65
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: EXTCONN, EXTCONN enumeration [COM], EXTCONN_CALLABLE, EXTCONN_STRONG, EXTCONN_WEAK, _com_EXTCONN, com.extconn, objidlbase/EXTCONN, objidlbase/EXTCONN_CALLABLE, objidlbase/EXTCONN_STRONG, objidlbase/EXTCONN_WEAK, tagEXTCONN
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: objidlbase.h
req.include-header: Objidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidlbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: EXTCONN
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - objidlbase.h
api_name:
 - EXTCONN
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagEXTCONN enumeration


## -description


Specifies the type of external connection existing on an embedded object. 


## -enum-fields




### -field EXTCONN_STRONG

The external connection is a link. If this value is specified, the external connection must keep the object alive until all strong external connections are cleared through <a href="https://msdn.microsoft.com/7ed598b2-9603-454a-99cf-849715e43ca1">IExternalConnection::ReleaseConnection</a>. 


### -field EXTCONN_WEAK

This value is not used.


### -field EXTCONN_CALLABLE

This value is not used.


## -see-also




<a href="https://msdn.microsoft.com/7439cb16-1da3-4fab-a16d-519f9ce1053a">IExternalConnection::AddConnection</a>



<a href="https://msdn.microsoft.com/7ed598b2-9603-454a-99cf-849715e43ca1">IExternalConnection::ReleaseConnection</a>
 

 

