---
UID: NF:dvbsiparser.IIsdbSIParameterDescriptor.GetLength
title: IIsdbSIParameterDescriptor::GetLength
author: windows-driver-content
description: Gets the body length of a service information (SI) parameter descriptor, in bytes.
old-location: mstv\iisdbsiparameterdescriptor_getlength.htm
old-project: mstv
ms.assetid: 6e4ac80d-30a9-4879-9cd3-a3964c675b27
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IIsdbSIParameterDescriptor interface, IIsdbSIParameterDescriptor interface [Microsoft TV Technologies],GetLength method, IIsdbSIParameterDescriptor.GetLength, IIsdbSIParameterDescriptor::GetLength, dvbsiparser/IIsdbSIParameterDescriptor::GetLength, mstv.iisdbsiparameterdescriptor_getlength
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IIsdbSIParameterDescriptor.GetLength
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbSIParameterDescriptor::GetLength


## -description


 Gets the body length of a service information (SI) parameter descriptor, in bytes. 


## -parameters




### -param pbVal [out]

Receives the descriptor length.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/264ae78d-cd72-49ff-b99b-2af637cc2917">IIsdbSIParameterDescriptor</a>
 

 

