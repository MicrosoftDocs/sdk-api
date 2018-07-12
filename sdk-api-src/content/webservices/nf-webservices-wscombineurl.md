---
UID: NF:webservices.WsCombineUrl
title: WsCombineUrl function
author: windows-sdk-content
description: Produces an absolute URL from a specified URL reference (absolute or relative URL) and a specified absolute base URL.
old-location: wsw\wscombineurl.htm
old-project: wsw
ms.assetid: 6cff906a-adb7-4453-8d44-6a5bf44a681b
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WsCombineUrl, WsCombineUrl function [Web Services for Windows], webservices/WsCombineUrl, wsw.wscombineurl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
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
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsCombineUrl
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsCombineUrl function


## -description




                Produces an absolute URL from a specified URL reference (absolute or relative URL) and a specified absolute base URL.




## -parameters




### -param baseUrl [in]

Pointer to a <a href="https://msdn.microsoft.com/2e771c56-4a07-4c8e-92c1-ffcbf74cd1aa">WS_STRING</a> structure containing an absolute URL in encoded format.
                


### -param referenceUrl [in]


                    Pointer to a <a href="https://msdn.microsoft.com/2e771c56-4a07-4c8e-92c1-ffcbf74cd1aa">WS_STRING</a> structure  containing an absolute or relative URL in encoded format.
                


### -param flags [in]

Controls the  format of the resulting URL.  For more information, see <a href="https://msdn.microsoft.com/b74c22fd-35b1-4d7b-974d-8ff7fff07813">WS_URL_FLAGS</a>.


### -param heap [in]

Pointer to the <a href="https://msdn.microsoft.com/1866f54f-26fc-4889-a88f-0d298a418bdc">WS_HEAP</a> object from which the memory for the resulting URL is allocated.
                


### -param resultUrl [out]

Pointer to a <a href="https://msdn.microsoft.com/2e771c56-4a07-4c8e-92c1-ffcbf74cd1aa">WS_STRING</a> structure that receives the resulting URL.
                This is an absolute URL in encoded format.
                


### -param error [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> structure  that receives additional error information if the function fails.
                


## -returns



If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">

One or more arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">

Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">

                    The base URL or reference URL was not in the correct format, or 
                    had a scheme that was not recognized.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>
 




## -remarks




                If the reference URL is absolute, it is returned unchanged, if the specified flags permit.
            If the reference URL is relative, it is combined with the base URL before being returned.
            


                Only the schemes listed in <a href="https://msdn.microsoft.com/e8763719-6ba0-4e5e-bb71-625d36a45eaf">WS_URL_SCHEME_TYPE</a> are supported.
            



