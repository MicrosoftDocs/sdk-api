---
UID: NC:winfax.PFAXFREEBUFFER
title: PFAXFREEBUFFER
author: windows-sdk-content
description: The FaxFreeBuffer function releases resources associated with a buffer allocated previously as the result of a function call by a fax client application.
old-location: fax\_mfax_faxfreebuffer.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_9xki.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FaxFreeBufferA, FaxFreeBufferW, PFAXFREEBUFFER, PFAXFREEBUFFER callback, PFAXFREEBUFFER callback function [Fax Service], _mfax_faxfreebuffer, fax._mfax_faxfreebuffer, winfax/FaxFreeBufferA, winfax/FaxFreeBufferW, winfax/PFAXFREEBUFFER
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxFreeBufferW (Unicode) and FaxFreeBufferA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winfax.h
api_name:
 - PFAXFREEBUFFER
 - FaxFreeBufferA
 - FaxFreeBufferW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFAXFREEBUFFER callback function


## -description


The <b>FaxFreeBuffer</b> function releases resources associated with a buffer allocated previously as the result of a function call by a fax client application. This includes calls to the <a href="https://msdn.microsoft.com/en-us/library/ms692819(v=VS.85).aspx">FaxCompleteJobParams</a> function and to functions that begin with <b>FaxEnum</b> or <b>FaxGet</b>.


## -parameters




### -param Buffer [in]

Type: <b>LPVOID</b>

Pointer to a buffer allocated on a previous call to one of the functions named in the following See Also section.


## -returns



This callback function does not return a value.




## -remarks



When the resources allocated for a buffer are no longer needed, the calling application must free the resources. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691947(v=VS.85).aspx">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692819(v=VS.85).aspx">FaxCompleteJobParams</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691941(v=VS.85).aspx">FaxEnumGlobalRoutingInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691958(v=VS.85).aspx">FaxEnumJobs</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690826(v=VS.85).aspx">FaxEnumPorts</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691804(v=VS.85).aspx">FaxEnumRoutingMethods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692282(v=VS.85).aspx">FaxGetConfiguration</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690909(v=VS.85).aspx">FaxGetDeviceStatus</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692186(v=VS.85).aspx">FaxGetJob</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691956(v=VS.85).aspx">FaxGetLoggingCategories</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691456(v=VS.85).aspx">FaxGetPageData</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691388(v=VS.85).aspx">FaxGetPort</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690904(v=VS.85).aspx">FaxGetRoutingInfo</a>
 

 

