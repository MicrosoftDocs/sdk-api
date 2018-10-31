---
UID: NF:strmif.IConfigInterleaving.put_Mode
title: IConfigInterleaving::put_Mode
author: windows-sdk-content
description: The put_Mode method sets how audio samples and video frames are to be written to disk, by specifying quality of interleaving.
old-location: dshow\iconfiginterleaving_put_mode.htm
tech.root: DirectShow
ms.assetid: 62b06dc2-2e71-4a14-82e5-63e921a3c11f
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IConfigInterleaving interface [DirectShow],put_Mode method, IConfigInterleaving.put_Mode, IConfigInterleaving::put_Mode, IConfigInterleavingput_Mode, dshow.iconfiginterleaving_put_mode, put_Mode, put_Mode method [DirectShow], put_Mode method [DirectShow],IConfigInterleaving interface, strmif/IConfigInterleaving::put_Mode
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
 - IConfigInterleaving.put_Mode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConfigInterleaving::put_Mode


## -description



The <code>put_Mode</code> method sets how audio samples and video frames are to be written to disk, by specifying quality of interleaving.




## -parameters




### -param mode [in]

Interleaving quality setting specified in the <a href="https://msdn.microsoft.com/4011b1e4-4bcf-4a2e-9d9a-ccdc8e12cd5a">InterleavingMode</a> enumeration.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/68594752-a711-4372-95db-10947bd2ce39">IConfigInterleaving Interface</a>



<a href="https://msdn.microsoft.com/02136798-1c49-4181-ad08-d128f580dbd4">IConfigInterleaving::get_Mode</a>
 

 

