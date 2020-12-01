---
UID: NC:winfax.PFAXFREEBUFFER
title: PFAXFREEBUFFER (winfax.h)
description: The FaxFreeBuffer function releases resources associated with a buffer allocated previously as the result of a function call by a fax client application.
helpviewer_keywords: ["FaxFreeBufferA","FaxFreeBufferW","PFAXFREEBUFFER","PFAXFREEBUFFER callback","PFAXFREEBUFFER callback function [Fax Service]","_mfax_faxfreebuffer","fax._mfax_faxfreebuffer","winfax/FaxFreeBufferA","winfax/FaxFreeBufferW","winfax/PFAXFREEBUFFER"]
old-location: fax\_mfax_faxfreebuffer.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_9xki.htm
ms.date: 12/05/2018
ms.keywords: FaxFreeBufferA, FaxFreeBufferW, PFAXFREEBUFFER, PFAXFREEBUFFER callback, PFAXFREEBUFFER callback function [Fax Service], _mfax_faxfreebuffer, fax._mfax_faxfreebuffer, winfax/FaxFreeBufferA, winfax/FaxFreeBufferW, winfax/PFAXFREEBUFFER
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFAXFREEBUFFER
 - winfax/PFAXFREEBUFFER
dev_langs:
 - c++
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
---

# PFAXFREEBUFFER callback function


## -description

The <b>FaxFreeBuffer</b> function releases resources associated with a buffer allocated previously as the result of a function call by a fax client application. This includes calls to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxcompletejobparamsa">FaxCompleteJobParams</a> function and to functions that begin with <b>FaxEnum</b> or <b>FaxGet</b>.

## -parameters

### -param Buffer [in]

Type: <b>LPVOID</b>

Pointer to a buffer allocated on a previous call to one of the functions named in the following See Also section.

## -remarks

When the resources allocated for a buffer are no longer needed, the calling application must free the resources. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-functions">Fax Service Client API Functions</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxcompletejobparamsa">FaxCompleteJobParams</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumglobalroutinginfoa">FaxEnumGlobalRoutingInfo</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumjobsa">FaxEnumJobs</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumportsa">FaxEnumPorts</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumroutingmethodsa">FaxEnumRoutingMethods</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetconfigurationa">FaxGetConfiguration</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetdevicestatusa">FaxGetDeviceStatus</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetjoba">FaxGetJob</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetloggingcategoriesa">FaxGetLoggingCategories</a>



<a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxgetpagedata">FaxGetPageData</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetporta">FaxGetPort</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetroutinginfoa">FaxGetRoutingInfo</a>