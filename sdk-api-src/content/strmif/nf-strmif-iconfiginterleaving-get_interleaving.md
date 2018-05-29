---
UID: NF:strmif.IConfigInterleaving.get_Interleaving
title: IConfigInterleaving::get_Interleaving
author: windows-sdk-content
description: The get_Interleaving method gets the audio preroll time and the frequency of interleaving for an AVI file.
old-location: dshow\iconfiginterleaving_get_interleaving.htm
old-project: DirectShow
ms.assetid: 659aa136-c7fd-4955-913b-26f7c05325a8
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IConfigInterleaving interface [DirectShow],get_Interleaving method, IConfigInterleaving.get_Interleaving, IConfigInterleaving::get_Interleaving, IConfigInterleavingget_Interleaving, dshow.iconfiginterleaving_get_interleaving, get_Interleaving, get_Interleaving method [DirectShow], get_Interleaving method [DirectShow],IConfigInterleaving interface, strmif/IConfigInterleaving::get_Interleaving
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IConfigInterleaving.get_Interleaving
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IConfigInterleaving::get_Interleaving


## -description



The <b>get_Interleaving</b> method gets the audio preroll time and the frequency of interleaving for an AVI file.




## -parameters




### -param prtInterleave [out]


            Receives the approximate duration of each interleaved group of audio or video chunks.


### -param prtPreroll [out]


            
            Receives the amount of audio data, in 100-nanosecond units, that is written to the file before the first video frame.
          
          


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



For more information, see <a href="https://msdn.microsoft.com/4b1363c4-9cdd-4b28-a5ea-e5e554597be2">IConfigInterleaving::put_Interleaving</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/68594752-a711-4372-95db-10947bd2ce39">IConfigInterleaving Interface</a>



<a href="https://msdn.microsoft.com/4b1363c4-9cdd-4b28-a5ea-e5e554597be2">IConfigInterleaving::put_Interleaving</a>
 

 

