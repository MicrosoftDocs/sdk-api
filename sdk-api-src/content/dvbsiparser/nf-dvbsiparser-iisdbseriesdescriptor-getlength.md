---
UID: NF:dvbsiparser.IIsdbSeriesDescriptor.GetLength
title: IIsdbSeriesDescriptor::GetLength method
author: windows-driver-content
description: Gets the body length of an Integrated Services Digital Broadcasting (ISDB) series descriptor, in bytes.
old-location: mstv\iisdbseriesdescriptor_getlength.htm
old-project: mstv
ms.assetid: 703e4406-7fca-4d96-83de-56fd2ff52d30
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies], IIsdbSeriesDescriptor interface, GetLength,IIsdbSeriesDescriptor.GetLength, IIsdbSeriesDescriptor, IIsdbSeriesDescriptor interface [Microsoft TV Technologies], GetLength method, IIsdbSeriesDescriptor::GetLength, dvbsiparser/IIsdbSeriesDescriptor::GetLength, mstv.iisdbseriesdescriptor_getlength
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
-	IIsdbSeriesDescriptor.GetLength
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbSeriesDescriptor::GetLength method


## -description


 Gets the body length of an Integrated Services Digital Broadcasting (ISDB) series descriptor, in bytes. 


## -parameters




### -param pbVal [out]

Receives the descriptor length.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/07c4debc-1817-46ac-9f67-9b8637a04662">IIsdbSeriesDescriptor</a>
 

 

