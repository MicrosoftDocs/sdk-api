---
UID: NF:amvideo.IQualProp.get_AvgSyncOffset
title: IQualProp::get_AvgSyncOffset
author: windows-sdk-content
description: The get_AvgSyncOffset method retrieves the average time difference between when the video frames should have been displayed and when they actually were.
old-location: dshow\iqualprop_get_avgsyncoffset.htm
tech.root: DirectShow
ms.assetid: 4bed68f0-d080-46d4-b582-e561ddca33f0
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IQualProp interface [DirectShow],get_AvgSyncOffset method, IQualProp.get_AvgSyncOffset, IQualProp::get_AvgSyncOffset, IQualPropget_AvgSyncOffset, amvideo/IQualProp::get_AvgSyncOffset, dshow.iqualprop_get_avgsyncoffset, get_AvgSyncOffset, get_AvgSyncOffset method [DirectShow], get_AvgSyncOffset method [DirectShow],IQualProp interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: amvideo.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IQualProp.get_AvgSyncOffset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IQualProp::get_AvgSyncOffset


## -description



The <code>get_AvgSyncOffset</code> method retrieves the average time difference between when the video frames should have been displayed and when they actually were.




## -parameters




### -param piAvg

Pointer to the time difference, expressed in milliseconds.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/428dfb97-0dfa-442c-819e-291e6a58f712">IQualProp Interface</a>
 

 

