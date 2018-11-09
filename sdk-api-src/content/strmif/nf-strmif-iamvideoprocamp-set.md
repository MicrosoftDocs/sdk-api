---
UID: NF:strmif.IAMVideoProcAmp.Set
title: IAMVideoProcAmp::Set
author: windows-sdk-content
description: The Set method sets video quality for a specified property.
old-location: dshow\iamvideoprocamp_set.htm
tech.root: DirectShow
ms.assetid: 18826377-ddf7-4c36-8995-43310ea077dd
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IAMVideoProcAmp interface [DirectShow],Set method, IAMVideoProcAmp.Set, IAMVideoProcAmp::Set, IAMVideoProcAmpSet, Set, Set method [DirectShow], Set method [DirectShow],IAMVideoProcAmp interface, dshow.iamvideoprocamp_set, strmif/IAMVideoProcAmp::Set
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMVideoProcAmp::Set


## -description



The <b>Set</b> method sets video quality for a specified property.




## -parameters




### -param Property [in]

The property to set, specified as a <a href="https://msdn.microsoft.com/113e3896-4920-41a3-9ce2-a26c34af4896">VideoProcAmpProperty</a> enumeration value.
          


### -param lValue [in]

The new value of the property.
          


### -param Flags [in]

The desired control setting, specified as a <a href="https://msdn.microsoft.com/42876f3b-d2b9-4ddb-85c0-80f5177eef6b">VideoProcAmpFlags</a> enumeration
          value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the <i>pCapsFlags</i> parameter is <b>VideoProcAmp_Flags_Auto</b>, the <i>lValue</i> parameter is ignored.




## -see-also




<a href="https://msdn.microsoft.com/f789db78-292e-4092-a5dc-1906845fb1dd">Configure the Video Quality</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/28c45790-2e5a-4acb-8a53-93f19c51dc6a">IAMVideoProcAmp Interface</a>



<a href="https://msdn.microsoft.com/8924383e-23e1-4732-9eff-dc7c8d0e361a">IAMVideoProcAmp::Get</a>
 

 

