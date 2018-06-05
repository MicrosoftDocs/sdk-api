---
UID: NF:dvbsiparser.IDvbLogicalChannelDescriptor.GetLength
title: IDvbLogicalChannelDescriptor::GetLength
author: windows-sdk-content
description: Note  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later. .
old-location: mstv\idvblogicalchanneldescriptor_getlength.htm
old-project: mstv
ms.assetid: 20c0f2a8-e4f5-4516-8c19-30cd19f0816e
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetLength, GetLength method [DirectShow], GetLength method [DirectShow],IDvbLogicalChannelDescriptor interface, IDvbLogicalChannelDescriptor interface [DirectShow],GetLength method, IDvbLogicalChannelDescriptor.GetLength, IDvbLogicalChannelDescriptor::GetLength, IDvbLogicalChannelDescriptorGetLength, dvbsiparser/IDvbLogicalChannelDescriptor::GetLength, mstv.idvblogicalchanneldescriptor_getlength
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDvbLogicalChannelDescriptor.GetLength
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbLogicalChannelDescriptor::GetLength


## -description




<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.</div>
<div> </div>




The <b>GetLength</b> method returns the length of the descriptor body.


## -parameters




### -param pbVal [out]


            Receives the length of the descriptor body, in bytes.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6e0a99e9-088f-420c-bb60-2d324aa28227">IDvbLogicalChannelDescriptor</a>
 

 

