---
UID: NF:strmif.IConfigInterleaving.get_Mode
title: IConfigInterleaving::get_Mode
author: windows-sdk-content
description: The get_Mode method retrieves the interleaving quality setting.
old-location: dshow\iconfiginterleaving_get_mode.htm
old-project: DirectShow
ms.assetid: 02136798-1c49-4181-ad08-d128f580dbd4
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: IConfigInterleaving interface [DirectShow],get_Mode method, IConfigInterleaving.get_Mode, IConfigInterleaving::get_Mode, IConfigInterleavingget_Mode, dshow.iconfiginterleaving_get_mode, get_Mode, get_Mode method [DirectShow], get_Mode method [DirectShow],IConfigInterleaving interface, strmif/IConfigInterleaving::get_Mode
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IConfigInterleaving.get_Mode
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IConfigInterleaving::get_Mode


## -description



The <code>get_Mode</code> method retrieves the interleaving quality setting.




## -parameters




### -param pMode [out]

Receives the interleaving quality, specified as a member of the <a href="https://msdn.microsoft.com/4011b1e4-4bcf-4a2e-9d9a-ccdc8e12cd5a">InterleavingMode</a> enumeration.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/68594752-a711-4372-95db-10947bd2ce39">IConfigInterleaving Interface</a>



<a href="https://msdn.microsoft.com/62b06dc2-2e71-4a14-82e5-63e921a3c11f">IConfigInterleaving::put_Mode</a>
 

 

