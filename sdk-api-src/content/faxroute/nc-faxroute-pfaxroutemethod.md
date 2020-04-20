---
UID: NC:faxroute.PFAXROUTEMETHOD
title: PFAXROUTEMETHOD (faxroute.h)
description: The FaxRouteMethod function is a placeholder for a function name defined by the fax routing extension DLL. This function executes a defined fax routing procedure.helpviewer_keywords: ["FaxRouteMethod","FaxRouteMethod callback","FaxRouteMethod callback function [Fax Service]","PFAXROUTEMETHOD","_mfax_faxroutemethod","fax._mfax_faxroutemethod","faxroute/FaxRouteMethod"]
old-location: fax\_mfax_faxroutemethod.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxrouteextapiref_2aw4.htm
ms.date: 12/05/2018
ms.keywords: FaxRouteMethod, FaxRouteMethod callback, FaxRouteMethod callback function [Fax Service], PFAXROUTEMETHOD, _mfax_faxroutemethod, fax._mfax_faxroutemethod, faxroute/FaxRouteMethod
f1_keywords:
- faxroute/FaxRouteMethod
dev_langs:
- c++
req.header: faxroute.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- FaxRoute.h
api_name:
- FaxRouteMethod
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PFAXROUTEMETHOD callback function


## -description


The <b>FaxRouteMethod</b> function is a placeholder for a function name defined by the fax routing extension DLL. This function executes a defined fax routing procedure.

The fax routing extension DLL can export multiple fax routing methods. The fax routing extension must export one uniquely named <b>FaxRouteMethod</b> function for each fax routing method it exports. It is recommended that each function name describe the functionality of the particular fax routing method. The fax service calls the <b>FaxRouteMethod</b> functions, in order of priority, after the service receives a fax document.


## -parameters




### -param *


### -param Arg1








#### - FailureData [out]

Type: <b>PVOID*</b>

Pointer to a variable that receives a pointer to a buffer that contains retry information for the fax routing method. This parameter can be equal to <b>NULL</b>. For more information, see the following Remarks section.


#### - FailureDataSize [out]

Type: <b>LPDWORD</b>

Pointer to an unsigned <b>DWORD</b> variable that receives the size, in bytes, of the buffer pointed to by the <i>FailureData</i> parameter.


#### - FaxRoute [in]

Type: <b>const <a href="https://msdn.microsoft.com/9cd01636-3b89-4b75-a3ef-317dd4b43c7a">FAX_ROUTE</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/9cd01636-3b89-4b75-a3ef-317dd4b43c7a">FAX_ROUTE</a> structure that contains information about the received fax document.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is a nonzero value.

                    

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, described in MSDN.




## -remarks



A fax routing method can manipulate the received Tagged Image File Format Class F (TIFF Class F) file. For example, one routing method could route the received Tagged Image File Format (TIFF) file to a specific destination such as a printer, or deliver the file in an email message to a user. Another routing method could convert the TIFF file to text using optical character recognition (OCR) technology, and then create a Microsoft Word document from the text. A fax routing method cannot delete or modify the TIFF file. For information about TIFF files, see <a href="https://msdn.microsoft.com/d7840c10-6059-40ed-9040-50eefefc7349">Fax Image Format</a>..

If you want the fax service to retry a failed routing method at a later time, the fax routing method must take the following steps.

<h3><a id="To_specify_that_the_fax_service_retry_a_fax_routing_method"></a><a id="to_specify_that_the_fax_service_retry_a_fax_routing_method"></a><a id="TO_SPECIFY_THAT_THE_FAX_SERVICE_RETRY_A_FAX_ROUTING_METHOD"></a>To specify that the fax service retry a fax routing method</h3>
<ol>
<li>Allocate a buffer to hold retry information for the fax routing method. The fax routing method must allocate the memory required for the buffer from the heap specified by the <a href="https://msdn.microsoft.com/6593762b-2a5a-4338-9958-efe0c7687729">FaxRouteInitialize</a> function.</li>
<li>Fill <i></i>the buffer with the information required to retry the fax routing method.</li>
<li>Set the <i>FailureData</i> parameter of the <b>FaxRouteMethod</b> function to a valid pointer value.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/9cd01636-3b89-4b75-a3ef-317dd4b43c7a">FAX_ROUTE</a>



<a href="https://msdn.microsoft.com/f8bdf0de-9455-45d1-9271-3929e0429d5c">Fax Routing Extension Application Programming Interface Overview</a>



<a href="https://msdn.microsoft.com/339f7fb6-64eb-403e-91be-210501042a25">Fax Routing Extension Functions</a>



<a href="https://msdn.microsoft.com/8c0e97ae-5d85-4271-a68a-7ad852b1615c">FaxRouteAddFile</a>



<a href="https://msdn.microsoft.com/44189520-42d9-4b1c-bb5a-f8da8bfc4c27">FaxRouteDeleteFile</a>



<a href="https://msdn.microsoft.com/779e7c8e-13b7-4495-b0b3-3b01594a88fb">FaxRouteEnumFiles</a>



<a href="https://msdn.microsoft.com/41acd3a8-269f-4c24-bb40-a8c5b24e1304">FaxRouteGetFile</a>



<a href="https://msdn.microsoft.com/6593762b-2a5a-4338-9958-efe0c7687729">FaxRouteInitialize</a>



<a href="https://msdn.microsoft.com/eeb84e95-1a47-4768-9cb7-d6e7a2ee2048">FaxRouteModifyRoutingData</a>
 

 

