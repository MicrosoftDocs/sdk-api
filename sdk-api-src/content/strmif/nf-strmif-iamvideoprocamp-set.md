---
UID: NF:strmif.IAMVideoProcAmp.Set
title: IAMVideoProcAmp::Set (strmif.h)
author: windows-sdk-content
description: The Set method sets video quality for a specified property.
old-location: dshow\iamvideoprocamp_set.htm
tech.root: DirectShow
ms.assetid: 18826377-ddf7-4c36-8995-43310ea077dd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMVideoProcAmp interface [DirectShow],Set method, IAMVideoProcAmp.Set, IAMVideoProcAmp::Set, IAMVideoProcAmpSet, Set, Set method [DirectShow], Set method [DirectShow],IAMVideoProcAmp interface, dshow.iamvideoprocamp_set, strmif/IAMVideoProcAmp::Set
ms.topic: method
f1_keywords: 
 - "strmif/IAMVideoProcAmp.Set"
dev_langs:
 - c++
req.header: strmif.h
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
 - IAMVideoProcAmp.Set
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMVideoProcAmp::Set


## -description



The <b>Set</b> method sets video quality for a specified property.




## -parameters




### -param Property [in]

The property to set, specified as a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-videoprocampproperty">VideoProcAmpProperty</a> enumeration value.
          


### -param lValue [in]

The new value of the property.
          


### -param Flags [in]

The desired control setting, specified as a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a> enumeration
          value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the <i>pCapsFlags</i> parameter is <b>VideoProcAmp_Flags_Auto</b>, the <i>lValue</i> parameter is ignored.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/configure-the-video-quality">Configure the Video Quality</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamvideoprocamp">IAMVideoProcAmp Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideoprocamp-get">IAMVideoProcAmp::Get</a>
 

 

