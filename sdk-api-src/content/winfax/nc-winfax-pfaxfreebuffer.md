---
UID: NC:winfax.PFAXFREEBUFFER
title: PFAXFREEBUFFER
author: windows-sdk-content
description: The FaxFreeBuffer function releases resources associated with a buffer allocated previously as the result of a function call by a fax client application.
old-location: fax\_mfax_faxfreebuffer.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_9xki.htm
ms.author: windowssdkdev
ms.date: 07/18/2018
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
tech.root: 
req.typenames: EVT_VARIANT, *PEVT_VARIANT
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PFAXFREEBUFFER callback function


## -description


The <b>FaxFreeBuffer</b> function releases resources associated with a buffer allocated previously as the result of a function call by a fax client application. This includes calls to the <a href="https://msdn.microsoft.com/46eb9960-1d07-4792-83d6-d2f5948e05e9">FaxCompleteJobParams</a> function and to functions that begin with <b>FaxEnum</b> or <b>FaxGet</b>.


## -parameters




### -param Buffer [in]

Type: <b>LPVOID</b>

Pointer to a buffer allocated on a previous call to one of the functions named in the following See Also section.


## -returns



This callback function does not return a value.




## -remarks



When the resources allocated for a buffer are no longer needed, the calling application must free the resources. For more information, see <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/b076b5ba-09af-4312-90c1-27abd0b859df">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/46eb9960-1d07-4792-83d6-d2f5948e05e9">FaxCompleteJobParams</a>



<a href="https://msdn.microsoft.com/776b1a16-9a5f-458b-96ee-b2f41568b7e5">FaxEnumGlobalRoutingInfo</a>



<a href="https://msdn.microsoft.com/d32cbef5-e548-4f66-bac6-c718c688547d">FaxEnumJobs</a>



<a href="https://msdn.microsoft.com/7bd33e6f-09ff-449b-ac22-b79a14e5d928">FaxEnumPorts</a>



<a href="https://msdn.microsoft.com/1f78fed5-6b49-4946-8607-f1d7f9052aaa">FaxEnumRoutingMethods</a>



<a href="https://msdn.microsoft.com/c29f0eaf-39a5-45e2-afb9-010494552969">FaxGetConfiguration</a>



<a href="https://msdn.microsoft.com/ddfba445-fdad-4fd8-b305-76d18b04583f">FaxGetDeviceStatus</a>



<a href="https://msdn.microsoft.com/784c4945-b4cc-446b-b0d4-c2fc58d46a9d">FaxGetJob</a>



<a href="https://msdn.microsoft.com/bcd650b3-92f3-4b3b-b4c2-c3418f914711">FaxGetLoggingCategories</a>



<a href="https://msdn.microsoft.com/81ff476c-ec10-406c-b89f-941ff6a491b7">FaxGetPageData</a>



<a href="https://msdn.microsoft.com/1cf89b9c-525d-42df-b3fa-4dda6f560fd6">FaxGetPort</a>



<a href="https://msdn.microsoft.com/c13d203d-e7b1-4bc6-a875-04ddd981d549">FaxGetRoutingInfo</a>
 

 

