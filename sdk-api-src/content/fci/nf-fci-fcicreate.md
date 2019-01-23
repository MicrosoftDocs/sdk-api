---
UID: NF:fci.FCICreate
title: FCICreate function
author: windows-sdk-content
description: The FCICreate function creates an FCI context.
old-location: winprog\fcicreate.htm
tech.root: DevNotes
ms.assetid: bfcea06d-2f09-405c-955c-0f56149148f2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FCICreate, FCICreate function [Windows API], fci/FCICreate, winprog.fcicreate
ms.topic: function
req.header: fci.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cabinet.lib
req.dll: Cabinet.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cabinet.dll
api_name:
 - FCICreate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FCICreate function


## -description


The <b>FCICreate</b> function creates an FCI context.


## -parameters




### -param perf [in, out]

Pointer to an <a href="https://msdn.microsoft.com/ddbccad9-a68c-4be7-90dc-e3dd25f5cf3b">ERF</a> structure that receives the error information.


### -param pfnfcifp [in]

Pointer to an application-defined callback function to notify when a file is placed in the cabinet. The function should be declared using the <a href="https://msdn.microsoft.com/f8a1bcfc-8a13-49cf-a3e7-caec6c6421b0">FNFCIFILEPLACED</a> macro.


### -param pfna [in]

Pointer to an application-defined callback function to allocate memory. The function should be declared using the <a href="https://msdn.microsoft.com/339ac9d2-60bc-4a90-8a46-6fbb073be9d1">FNFCIALLOC</a> macro.


### -param pfnf [in]

Pointer to an application-defined callback function to free previously allocated memory. The function should be delcared using the <a href="https://msdn.microsoft.com/48f052e2-7786-430a-b3dc-afcfdffae387">FNFCIFREE</a> macro.


### -param pfnopen [in]

Pointer to an application-defined callback function to open a file. The function should be declared using the <a href="https://msdn.microsoft.com/72cf50cb-c895-4953-9c4d-f8ddaa294f2a">FNFCIOPEN</a> macro.


### -param pfnread [in]

Pointer to an application-defined callback function to read data from a file. The function should be declared using the <a href="https://msdn.microsoft.com/dd4e97ff-efbc-462b-b954-bc3260fa1513">FNFCIREAD</a> macro.


### -param pfnwrite [in]

Pointer to an application-defined callback function to write data to a file. The function should be declared using the <a href="https://msdn.microsoft.com/ca4c3b5b-1ed5-4f12-8317-c1e1dac5f816">FNFCIWRITE</a> macro.


### -param pfnclose [in]

Pointer to an application-defined callback function to close a file. The function should be declared using the <a href="https://msdn.microsoft.com/c4edf6ca-0b16-4e30-933b-934f8930c6d6">FNFCICLOSE</a> macro.


### -param pfnseek [in]

Pointer to an application-defined callback function to move a file pointer to the specific location. The function should be declared using the <a href="https://msdn.microsoft.com/e5a14c98-4de6-452e-8993-afb7964aeee7">FNFCISEEK</a> macro.


### -param pfndelete [in]

Pointer to an application-defined callback function to delete a file. The function should be declared using the <a href="https://msdn.microsoft.com/5c85ad86-2794-4f7c-8c10-18fea3519b11">FNFCIDELETE</a> macro.


### -param pfnfcigtf [in]

Pointer to an application-defined callback function to retrieve a temporary file name. The function should be declared using the <a href="https://msdn.microsoft.com/8978f688-d8f1-437a-b298-eed1e7dac012">FNFCIGETTEMPFILE</a> macro.


### -param pccab [in]

Pointer to a <a href="https://msdn.microsoft.com/e25cb72b-4c96-40e9-9fd5-2920e4a01d3a">CCAB</a> structure that contains the parameters for creating a cabinet.


### -param pv [in, optional]

Pointer to an application-defined value that is passed to callback functions.


## -returns



If the function succeeds, it returns a non-<b>NULL</b> HFCI context pointer; otherwise, <b>NULL</b>.

Extended error information is provided in the <a href="https://msdn.microsoft.com/ddbccad9-a68c-4be7-90dc-e3dd25f5cf3b">ERF</a> structure.




## -remarks



FCI supports multiple simultaneous contexts. As a result it is possible to create or extract multiple cabinets at the same time within the same application. If the application is multithreaded, it is also possible to run a different context in each thread; however, an application cannot use the same context simultaneously in multiple threads. For example, <a href="https://msdn.microsoft.com/f99e8718-853b-4d35-98ae-61a8333dbaba">FCIAddFile</a> cannot be called from two different threads, using the same FCI context.




## -see-also




<a href="https://msdn.microsoft.com/f99e8718-853b-4d35-98ae-61a8333dbaba">FCIAddFile</a>



<a href="https://msdn.microsoft.com/bb1a6294-664f-450f-b8ec-d6f8957d920e">FCIDestroy</a>



<a href="https://msdn.microsoft.com/dc9c226e-e309-48c3-9edb-3f0a040c0c18">FCIFlushFolder</a>
 

 

