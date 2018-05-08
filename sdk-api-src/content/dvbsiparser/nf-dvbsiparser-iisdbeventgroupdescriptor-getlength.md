---
UID: NF:dvbsiparser.IIsdbEventGroupDescriptor.GetLength
title: IIsdbEventGroupDescriptor::GetLength
author: windows-driver-content
description: Gets the body length of an Integrated Services Digital Broadcasting (ISDB) event group descriptor, in bytes.
old-location: mstv\iisdbeventgroupdescriptor_getlength.htm
old-project: mstv
ms.assetid: 08e61ddb-15d5-40e3-9e37-7c45d1f18b4a
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IIsdbEventGroupDescriptor interface, IIsdbEventGroupDescriptor interface [Microsoft TV Technologies],GetLength method, IIsdbEventGroupDescriptor.GetLength, IIsdbEventGroupDescriptor::GetLength, dvbsiparser/IIsdbEventGroupDescriptor::GetLength, mstv.iisdbeventgroupdescriptor_getlength
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
-	IIsdbEventGroupDescriptor.GetLength
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbEventGroupDescriptor::GetLength


## -description


 Gets the body length of an Integrated Services Digital Broadcasting (ISDB) event group descriptor, in bytes. 


## -parameters




### -param pbVal [out]

Receives the descriptor length.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1e71f277-0296-4589-8099-dfae2a9dcfb0">IIsdbEventGroupDescriptor</a>
 

 

