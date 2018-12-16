---
UID: NF:dxgidebug.IDXGIDebug.ReportLiveObjects
title: IDXGIDebug::ReportLiveObjects
author: windows-sdk-content
description: Reports info about the lifetime of an object or objects.
old-location: direct3ddxgi\idxgidebug_reportliveobjects.htm
tech.root: direct3ddxgi
ms.assetid: 6CA5C335-08E3-4CC6-A9C9-D7BC6B11C0EA
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDXGIDebug interface [DXGI],ReportLiveObjects method, IDXGIDebug.ReportLiveObjects, IDXGIDebug::ReportLiveObjects, ReportLiveObjects, ReportLiveObjects method [DXGI], ReportLiveObjects method [DXGI],IDXGIDebug interface, direct3ddxgi.idxgidebug_reportliveobjects, dxgidebug/IDXGIDebug::ReportLiveObjects
ms.topic: method
req.header: dxgidebug.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: DXGIDebug.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGIDebug.dll
api_name:
 - IDXGIDebug.ReportLiveObjects
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIDebug::ReportLiveObjects


## -description


Reports info about the lifetime of an object or objects.


## -parameters




### -param apiid

The globally unique identifier (GUID) of the object or objects to get info about. Use one of the <a href="https://msdn.microsoft.com/85946D30-5E49-4E4B-AC25-394ABFF0DB11">DXGI_DEBUG_ID</a> GUIDs.


### -param flags

A <a href="https://msdn.microsoft.com/8A4B4139-42FC-4983-9699-ABCDBF5783E7">DXGI_DEBUG_RLO_FLAGS</a>-typed value that specifies the amount of info to report.


## -returns



Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a>.




## -remarks



<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/7DCA4750-A397-4B5A-908F-A046427D30FB">IDXGIDebug</a>
 

 

