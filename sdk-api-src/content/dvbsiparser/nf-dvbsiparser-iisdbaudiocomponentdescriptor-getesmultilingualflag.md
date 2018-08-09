---
UID: NF:dvbsiparser.IIsdbAudioComponentDescriptor.GetESMultiLingualFlag
title: IIsdbAudioComponentDescriptor::GetESMultiLingualFlag
author: windows-sdk-content
description: Gets a flag from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor that indicates whether the stream uses ES multilingual mode.
old-location: mstv\iisdbaudiocomponentdescriptor_getesmultilingualflag.htm
old-project: mstv
ms.assetid: 10a47ca7-84db-48de-8ba5-0be257438044
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetESMultiLingualFlag, GetESMultiLingualFlag method [Microsoft TV Technologies], GetESMultiLingualFlag method [Microsoft TV Technologies],IIsdbAudioComponentDescriptor interface, IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies],GetESMultiLingualFlag method, IIsdbAudioComponentDescriptor.GetESMultiLingualFlag, IIsdbAudioComponentDescriptor::GetESMultiLingualFlag, dvbsiparser/IIsdbAudioComponentDescriptor::GetESMultiLingualFlag, mstv.iisdbaudiocomponentdescriptor_getesmultilingualflag
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IIsdbAudioComponentDescriptor.GetESMultiLingualFlag
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbAudioComponentDescriptor::GetESMultiLingualFlag


## -description


Gets a flag  from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor that indicates whether the stream uses ES multilingual mode. 


## -parameters




### -param pfVal [out]

Receives 1 if the stream uses ES multilingual mode. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



ES multilingual mode (also called <i>2-language multilingual mode</i> or <i>1/0  + 1/0 mode</i>) is a dual-channel monaural mode indicated by a value of 0x02 in the component_type field of the descriptor.




## -see-also




<a href="https://msdn.microsoft.com/f771b318-5fd5-4c7f-a22b-6966aec5c0fa">IIsdbAudioComponentDescriptor</a>
 

 

