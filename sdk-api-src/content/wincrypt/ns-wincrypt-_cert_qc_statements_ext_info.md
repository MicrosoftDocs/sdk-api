---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _CERT_QC_STATEMENTS_EXT_INFO structure


## -description


The <b>CERT_QC_STATEMENTS_EXT_INFO</b> structure contains a sequence of one or more statements that make up the Qualified Certificate (QC) statements extension for a QC.


## -struct-fields




### -field cStatement

A value that represents the size, in bytes, of the <b>rgStatement</b> array.


### -field rgStatement

An array of <a href="https://msdn.microsoft.com/e163da81-d854-4f56-8eef-2788f1b566ba">CERT_QC_STATEMENT</a> structures that contains the sequence of statements that make up the QC statements extension.


## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=104367">RFC 3280</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=104368">RFC 3739</a>
 

 

