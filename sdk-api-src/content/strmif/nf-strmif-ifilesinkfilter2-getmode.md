---
UID: NF:strmif.IFileSinkFilter2.GetMode
title: IFileSinkFilter2::GetMode
author: windows-sdk-content
description: The GetMode method retrieves whether the file writer destroys the file when it creates the new one.
old-location: dshow\ifilesinkfilter2_getmode.htm
tech.root: DirectShow
ms.assetid: b2a8e34e-a6c1-448b-be6e-31fba9d64f6e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetMode, GetMode method [DirectShow], GetMode method [DirectShow],IFileSinkFilter2 interface, IFileSinkFilter2 interface [DirectShow],GetMode method, IFileSinkFilter2.GetMode, IFileSinkFilter2::GetMode, IFileSinkFilter2GetMode, dshow.ifilesinkfilter2_getmode, strmif/IFileSinkFilter2::GetMode
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
 - IFileSinkFilter2.GetMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileSinkFilter2::GetMode


## -description



The <code>GetMode</code> method retrieves whether the file writer destroys the file when it creates the new one.




## -parameters




### -param pdwFlags [out]

Pointer to the retrieved flags. Currently, the only defined flag is AM_FILE_OVERWRITE, which indicates that the file should be destroyed; zero indicates that the file will be left alone.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/1339c441-2b10-461f-87f3-4835c1692740">IFileSinkFilter2 Interface</a>
 

 

