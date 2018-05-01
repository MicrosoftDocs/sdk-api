---
UID: NF:strmif.IFileSinkFilter2.SetMode
title: IFileSinkFilter2::SetMode method
author: windows-driver-content
description: The SetMode method determines whether the file writer destroys the file when it creates the new one.
old-location: dshow\ifilesinkfilter2_setmode.htm
old-project: DirectShow
ms.assetid: a32ae597-1468-4ac8-ae7b-8831d2a9ad6e
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IFileSinkFilter2, IFileSinkFilter2 interface [DirectShow], SetMode method, IFileSinkFilter2::SetMode, IFileSinkFilter2SetMode, SetMode method [DirectShow], SetMode method [DirectShow], IFileSinkFilter2 interface, SetMode,IFileSinkFilter2.SetMode, dshow.ifilesinkfilter2_setmode, strmif/IFileSinkFilter2::SetMode
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
-	IFileSinkFilter2.SetMode
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IFileSinkFilter2::SetMode method


## -description



The <code>SetMode</code> method determines whether the file writer destroys the file when it creates the new one.




## -parameters




### -param dwFlags [in]

Currently, the only defined flag is AM_FILE_OVERWRITE, which indicates that the file writer should destroy the file. Specify zero for <i>dwFlags</i> to leave the file alone.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/1339c441-2b10-461f-87f3-4835c1692740">IFileSinkFilter2 Interface</a>
 

 

