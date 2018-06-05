---
UID: NN:dxgidebug.IDXGIDebug
title: IDXGIDebug
author: windows-sdk-content
description: This interface controls debug settings, and can only be used if the debug layer is turned on.
old-location: direct3ddxgi\idxgidebug.htm
old-project: direct3ddxgi
ms.assetid: 7DCA4750-A397-4B5A-908F-A046427D30FB
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: IDXGIDebug, IDXGIDebug interface [DXGI], IDXGIDebug interface [DXGI],described, direct3ddxgi.idxgidebug, dxgidebug/IDXGIDebug
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dxgidebug.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
req.typenames: DXGI_INFO_QUEUE_MESSAGE_SEVERITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DXGIDebug.dll
api_name:
-	IDXGIDebug
product: Windows
targetos: Windows
req.lib: 
req.dll: DXGIDebug.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIDebug interface


## -description


This interface controls debug settings, and can only be used if the debug layer is turned on.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIDebug</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDXGIDebug</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIDebug</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6CA5C335-08E3-4CC6-A9C9-D7BC6B11C0EA">ReportLiveObjects</a>
</td>
<td align="left" width="63%">
Reports info about the lifetime of an object or objects.

</td>
</tr>
</table> 


## -remarks




          This interface is obtained by calling the <a href="https://msdn.microsoft.com/7702B842-6808-4CA9-A5B4-B1A1DC2479A7">DXGIGetDebugInterface</a> function.
        


          For more info about the debug layer, see <a href="https://msdn.microsoft.com/c545983c-5351-42a9-82e5-deea73aa035f">Debug Layer</a>.
        

<b>Windows Phone 8:
        </b> This API is supported.
      

<div class="alert"><b>Note</b>  
        This API requires the Windows Software Development Kit (SDK) for Windows 8.
      </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

