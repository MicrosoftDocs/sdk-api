---
UID: NS:winfax._FAX_CONTEXT_INFOW
title: "_FAX_CONTEXT_INFOW"
author: windows-sdk-content
description: The FAX_CONTEXT_INFO structure contains information about a fax printer device context. The SizeOfStruct member is required. Information for the other members is supplied by a call to the FaxStartPrintJob function.
old-location: fax\_mfax_fax_context_info_str.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_7v5e.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: "*PFAX_CONTEXT_INFOW, FAX_CONTEXT_INFO, FAX_CONTEXT_INFO structure [Fax Service], FAX_CONTEXT_INFOA, FAX_CONTEXT_INFOW, PFAX_CONTEXT_INFO, PFAX_CONTEXT_INFO structure pointer [Fax Service], _FAX_CONTEXT_INFOW, _mfax_fax_context_info_str, fax._mfax_fax_context_info_str, winfax/FAX_CONTEXT_INFO, winfax/FAX_CONTEXT_INFOA, winfax/FAX_CONTEXT_INFOW, winfax/PFAX_CONTEXT_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FAX_CONTEXT_INFOW (Unicode) and FAX_CONTEXT_INFOA (ANSI)
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
 - HeaderDef
api_location:
 - Winfax.h
api_name:
 - FAX_CONTEXT_INFO
 - FAX_CONTEXT_INFOA
 - FAX_CONTEXT_INFOW
product: Windows
targetos: Windows
req.typenames: FAX_CONTEXT_INFOW, *PFAX_CONTEXT_INFOW
req.redist: 
---

# _FAX_CONTEXT_INFOW structure


## -description


The <b>FAX_CONTEXT_INFO</b> structure contains information about a fax printer device context. The <b>SizeOfStruct</b> member is required. Information for the other members is supplied by a call to the <a href="https://msdn.microsoft.com/219cc7f7-d5c8-416b-b9ea-0f13584cac57">FaxStartPrintJob</a> function.


## -struct-fields




### -field SizeOfStruct

Type: <b>DWORD</b>

Specifies the size, in bytes, of the <b>FAX_CONTEXT_INFO</b> structure. The calling application must set this member to <b>sizeof(FAX_CONTEXT_INFO)</b> before it calls the <a href="https://msdn.microsoft.com/219cc7f7-d5c8-416b-b9ea-0f13584cac57">FaxStartPrintJob</a> function.


### -field hDC

Type: <b>HDC</b>

Handle to a fax printer device context. A call to the <a href="https://msdn.microsoft.com/219cc7f7-d5c8-416b-b9ea-0f13584cac57">FaxStartPrintJob</a> function supplies the data for this member.


### -field ServerName

Type: <b>TCHAR[MAX_COMPUTERNAME_LENGTH+1]</b>

Specifies a variable that contains a null-terminated string that is the fax server name of interest. A call to the <a href="https://msdn.microsoft.com/219cc7f7-d5c8-416b-b9ea-0f13584cac57">FaxStartPrintJob</a> function supplies the data for this member. If the fax server is on the local computer, this member will be empty. The client application does not need to fill in this member.


## -remarks



A fax client application can call the <a href="https://msdn.microsoft.com/219cc7f7-d5c8-416b-b9ea-0f13584cac57">FaxStartPrintJob</a> function to retrieve the handle to a fax printer device context. The function returns the handle in a <b>FAX_CONTEXT_INFO</b> structure. The application must call the <a href="_win32_DeleteDC">DeleteDC</a> function to deallocate the handle to the printer device context. For more information, see <a href="https://msdn.microsoft.com/d6e0afbd-6e64-487c-97fc-1e5cd5092d14">Printing a Fax to a Device Context</a>.




## -see-also




<a href="_win32_DeleteDC">DeleteDC</a>



<a href="_win32_EndDoc">EndDoc</a>



<a href="https://msdn.microsoft.com/be81e221-4aba-4c63-9640-337bee49fdb4">Fax Service Client API Structures</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/a48d4eb2-2b49-4379-a281-e5465de1af94">FaxPrintCoverPage</a>



<a href="https://msdn.microsoft.com/219cc7f7-d5c8-416b-b9ea-0f13584cac57">FaxStartPrintJob</a>
 

 

