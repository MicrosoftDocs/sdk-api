---
UID: NE:photoacquire.tagERROR_ADVISE_RESULT
title: ERROR_ADVISE_RESULT (photoacquire.h)
description: The ERROR_ADVISE_RESULT enumeration type indicates the type of error values that can be assigned to the pnErrorAdviseResult parameter of IPhotoAcquireProgressCB::ErrorAdvise.
helpviewer_keywords: ["ERROR_ADVISE_RESULT","ERROR_ADVISE_RESULT enumeration [Picture Acquisition]","PHOTOACQUIRE_RESULT_ABORT","PHOTOACQUIRE_RESULT_NO","PHOTOACQUIRE_RESULT_OK","PHOTOACQUIRE_RESULT_RETRY","PHOTOACQUIRE_RESULT_SKIP","PHOTOACQUIRE_RESULT_SKIP_ALL","PHOTOACQUIRE_RESULT_YES","enumeration [Picture Acquisition]","photoacquire/ERROR_ADVISE_RESULT","photoacquire/PHOTOACQUIRE_RESULT_ABORT","photoacquire/PHOTOACQUIRE_RESULT_NO","photoacquire/PHOTOACQUIRE_RESULT_OK","photoacquire/PHOTOACQUIRE_RESULT_RETRY","photoacquire/PHOTOACQUIRE_RESULT_SKIP","photoacquire/PHOTOACQUIRE_RESULT_SKIP_ALL","photoacquire/PHOTOACQUIRE_RESULT_YES","picacq.error_advise_result"]
old-location: picacq\error_advise_result.htm
tech.root: picacq
ms.assetid: a3cb2a2d-049a-4607-beaf-41ea6f0d4704
ms.date: 12/05/2018
ms.keywords: ERROR_ADVISE_RESULT, ERROR_ADVISE_RESULT enumeration [Picture Acquisition], PHOTOACQUIRE_RESULT_ABORT, PHOTOACQUIRE_RESULT_NO, PHOTOACQUIRE_RESULT_OK, PHOTOACQUIRE_RESULT_RETRY, PHOTOACQUIRE_RESULT_SKIP, PHOTOACQUIRE_RESULT_SKIP_ALL, PHOTOACQUIRE_RESULT_YES, enumeration [Picture Acquisition], photoacquire/ERROR_ADVISE_RESULT, photoacquire/PHOTOACQUIRE_RESULT_ABORT, photoacquire/PHOTOACQUIRE_RESULT_NO, photoacquire/PHOTOACQUIRE_RESULT_OK, photoacquire/PHOTOACQUIRE_RESULT_RETRY, photoacquire/PHOTOACQUIRE_RESULT_SKIP, photoacquire/PHOTOACQUIRE_RESULT_SKIP_ALL, photoacquire/PHOTOACQUIRE_RESULT_YES, picacq.error_advise_result
req.header: photoacquire.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ERROR_ADVISE_RESULT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagERROR_ADVISE_RESULT
 - photoacquire/tagERROR_ADVISE_RESULT
 - ERROR_ADVISE_RESULT
 - photoacquire/ERROR_ADVISE_RESULT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - PhotoAcquire.h
api_name:
 - ERROR_ADVISE_RESULT
---

# ERROR_ADVISE_RESULT enumeration


## -description

The <code>ERROR_ADVISE_RESULT</code> enumeration type indicates the type of error values that can be assigned to the <i>pnErrorAdviseResult</i> parameter of <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-erroradvise">IPhotoAcquireProgressCB::ErrorAdvise</a>.

## -enum-fields

### -field PHOTOACQUIRE_RESULT_YES:0

Specifies a Yes response to an error dialog. Valid only if the <i>nMessageType</i> parameter to <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-erroradvise">IPhotoAcquireProgressCB::ErrorAdvise</a> is PHOTOACQUIRE_ERROR_YESNO.

### -field PHOTOACQUIRE_RESULT_NO:1

Specifies a No response to an error dialog. Valid only if the <i>nMessageType</i> parameter to <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-erroradvise">IPhotoAcquireProgressCB::ErrorAdvise</a> is PHOTOACQUIRE_ERROR_YESNO.

### -field PHOTOACQUIRE_RESULT_OK:2

Specifies an OK response to an error dialog. Valid only if the <i>nMessageType</i> parameter to <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-erroradvise">IPhotoAcquireProgressCB::ErrorAdvise</a> is PHOTOACQUIRE_ERROR_OK.

### -field PHOTOACQUIRE_RESULT_SKIP:3

Specifies a Skip response to an error dialog. Valid only if the <i>nMessageType</i> parameter to <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-erroradvise">IPhotoAcquireProgressCB::ErrorAdvise</a> is PHOTOACQUIRE_ERROR_SKIPRETRYCANCEL.

### -field PHOTOACQUIRE_RESULT_SKIP_ALL:4

Specifies a Skip All response to an error dialog. Valid only if the <i>nMessageType</i> parameter to <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-erroradvise">IPhotoAcquireProgressCB::ErrorAdvise</a> is PHOTOACQUIRE_ERROR_SKIPRETRYCANCEL.

### -field PHOTOACQUIRE_RESULT_RETRY:5

Specifies a Retry response to an error dialog. Valid only if the <i>nMessageType</i> parameter to <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-erroradvise">IPhotoAcquireProgressCB::ErrorAdvise</a> is PHOTOACQUIRE_ERROR_SKIPRETRYCANCEL or PHOTOACQUIRE_ERROR_RETRYCANCEL.

### -field PHOTOACQUIRE_RESULT_ABORT:6

Specifies a Cancel response to an error dialog. Valid only if the <i>nMessageType</i> parameter to <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-erroradvise">IPhotoAcquireProgressCB::ErrorAdvise</a> is PHOTOACQUIRE_ERROR_SKIPRETRYCANCEL or PHOTOACQUIRE_ERROR_RETRYCANCEL.

## -remarks

The type of response allowed is of type <a href="/windows/win32/api/photoacquire/ne-photoacquire-error_advise_message_type">ERROR_ADVISE_MESSAGE_TYPE</a>, and indicated by the <i>nMessageType</i> parameter of <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-erroradvise">IPhotoAcquireProgressCB::ErrorAdvise</a>.

## -see-also

<a href="/windows/win32/api/photoacquire/ne-photoacquire-error_advise_message_type">ERROR_ADVISE_MESSAGE_TYPE</a>



<a href="/previous-versions/windows/desktop/acquisition/enumeration-types">Enumeration Types</a>



<a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-erroradvise">IPhotoAcquireProgressCB::ErrorAdvise</a>
