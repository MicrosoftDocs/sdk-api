---
UID: NF:strmif.IDistributorNotify.Run
title: IDistributorNotify::Run
author: windows-sdk-content
description: The Run method is called when the filter graph is entering a running state.
old-location: dshow\idistributornotify_run.htm
tech.root: DirectShow
ms.assetid: d6a6595b-b243-41bf-bba9-6e35fa81116c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDistributorNotify interface [DirectShow],Run method, IDistributorNotify.Run, IDistributorNotify::Run, IDistributorNotifyRun, Run, Run method [DirectShow], Run method [DirectShow],IDistributorNotify interface, dshow.idistributornotify_run, strmif/IDistributorNotify::Run
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
 - IDistributorNotify.Run
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDistributorNotify::Run


## -description



The <code>Run</code> method is called when the filter graph is entering a running state.




## -parameters




### -param tStart

Stream-time offset that will be passed to every filter's <a href="https://msdn.microsoft.com/ec422312-bbc2-4b66-b2cd-1a9eebd1eee1">IMediaFilter::Run</a> method.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method is called before the filters are notified.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/c7c9ee95-9d68-45c5-a3ca-8d6071782851">IDistributorNotify Interface</a>
 

 

