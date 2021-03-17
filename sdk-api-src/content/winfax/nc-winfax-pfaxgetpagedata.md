---
UID: NC:winfax.PFAXGETPAGEDATA
title: PFAXGETPAGEDATA (winfax.h)
description: The FaxGetPageData function returns to a fax client application the first page of data for a fax job.
helpviewer_keywords: ["FaxGetPageDataA","FaxGetPageDataW","PFAXGETPAGEDATA","PFAXGETPAGEDATA callback","PFAXGETPAGEDATA callback function [Fax Service]","_mfax_faxgetpagedata","fax._mfax_faxgetpagedata","winfax/FaxGetPageDataA","winfax/FaxGetPageDataW","winfax/PFAXGETPAGEDATA"]
old-location: fax\_mfax_faxgetpagedata.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3ko1.htm
ms.date: 12/05/2018
ms.keywords: FaxGetPageDataA, FaxGetPageDataW, PFAXGETPAGEDATA, PFAXGETPAGEDATA callback, PFAXGETPAGEDATA callback function [Fax Service], _mfax_faxgetpagedata, fax._mfax_faxgetpagedata, winfax/FaxGetPageDataA, winfax/FaxGetPageDataW, winfax/PFAXGETPAGEDATA
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxGetPageDataW (Unicode) and FaxGetPageDataA (ANSI)
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
 - PFAXGETPAGEDATA
 - winfax/PFAXGETPAGEDATA
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
 - PFAXGETPAGEDATA
 - FaxGetPageDataA
 - FaxGetPageDataW
---

# PFAXGETPAGEDATA callback function


## -description

The <b>FaxGetPageData</b> function returns to a fax client application the first page of data for a fax job. The fax job must be an outbound job, but it can be queued or active. The function returns data in the Tagged Image File Format Class F (TIFF Class F) format.

## -parameters

### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a> function.

### -param JobId [in]

Type: <b>DWORD</b>

Specifies a unique number that identifies the fax job associated with the page of data.

### -param Buffer [out]

Type: <b>LPBYTE*</b>

Pointer to the address of a buffer to receive the first page of data in the fax document. For information about memory allocation, see the following Remarks section.

### -param BufferSize [out]

Type: <b>LPDWORD</b>

Pointer to a <b>DWORD</b> variable to receive the size of the buffer, in bytes, pointed to by the <i>Buffer</i> parameter.

### -param ImageWidth [out]

Type: <b>LPDWORD</b>

Pointer to a <b>DWORD</b> variable to receive the width, in pixels, of the fax image.

### -param ImageHeight [out]

Type: <b>LPDWORD</b>

Pointer to a <b>DWORD</b> variable to receive the height, in pixels, of the fax image.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. GetLastError can return one of the following errors.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. <a href="/previous-versions/windows/desktop/fax/-mfax-specific-fax-access-rights">FAX_JOB_QUERY</a> access is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or all of the <i>Buffer</i>, <i>BufferSize</i>, <i>ImageWidth</i>, <i>ImageHeight</i>, or <i>FaxHandle</i> parameters are <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
An error occurred during memory allocation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
An invalid-data error occurred. For example, the fax job identified by the <i>JobId</i> parameter is not an outgoing fax transmission; the job must be specified with the JT_SEND job type.

</td>
</tr>
</table>

## -remarks

A fax client application can call the <b>FaxGetPageData</b> function for administrative purposes, to display a thumbnail sketch of the fax documents in the fax queue.

The fax service creates fax documents as TIFF Class F files based on the Tagged Image File Format (TIFF) 6.0 specification. The <b>FaxGetPageData</b> function returns a TIFF data stream that has a Modified Modified READ (MMR) two-dimensional encoding data compression format. The calling application must decode the data stream. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-fax-image-format">Fax Image Format</a>.

The <b>FaxGetPageData</b> function allocates the memory required for the <i>Buffer</i> parameter. An application must call the <a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxfreebuffer">FaxFreeBuffer</a> function to deallocate the resources associated with this parameter.

For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-displaying-documents-in-the-fax-job-queue">Displaying Documents in the Fax Job Queue</a> and <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-functions">Fax Service Client API Functions</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a>



<a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxfreebuffer">FaxFreeBuffer</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxprintcoverpagea">FaxPrintCoverPage</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxstartprintjoba">FaxStartPrintJob</a>
