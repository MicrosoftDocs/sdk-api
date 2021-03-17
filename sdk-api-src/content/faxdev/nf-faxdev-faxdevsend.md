---
UID: NF:faxdev.FaxDevSend
title: FaxDevSend function (faxdev.h)
description: The fax service calls the FaxDevSend function to signal a fax service provider (FSP) that it must initiate an outgoing fax transmission. Each FSP must export the FaxDevSend function.
helpviewer_keywords: ["FaxDevSend","FaxDevSend function [Fax Service]","_mfax_faxdevsend","fax._mfax_faxdevsend","faxdev/FaxDevSend"]
old-location: fax\_mfax_faxdevsend.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxfspapiref_7rz8.htm
ms.date: 12/05/2018
ms.keywords: FaxDevSend, FaxDevSend function [Fax Service], _mfax_faxdevsend, fax._mfax_faxdevsend, faxdev/FaxDevSend
req.header: faxdev.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FaxDevSend
 - faxdev/FaxDevSend
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - FaxDev.h
api_name:
 - FaxDevSend
---

# FaxDevSend function


## -description

The fax service calls the <b>FaxDevSend</b> function to signal a fax service provider (FSP) that it must initiate an outgoing fax transmission. Each FSP must export the <b>FaxDevSend</b> function.

## -parameters

### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax handle returned by the <a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevstartjob">FaxDevStartJob</a> function.

### -param FaxSend [in]

Type: <b>PFAX_SEND</b>

Pointer to a <a href="/windows/desktop/api/faxdev/ns-faxdev-fax_send">FAX_SEND</a> structure that contains the sending information. For more information, see the following Remarks section.

### -param FaxSendCallback

Type: <b>PFAX_SEND_CALLBACK</b>

Pointer to a callback function that notifies the fax service of the call handle that TAPI assigns. For more information, see the following Remarks section.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<div class="alert"><b>Note</b>  For a successful send, FaxDevSend() should return <b>TRUE</b> and FaxDevReportStatus() should return FS_COMPLETED. For an unsuccessful send, FaxDevSend() should return <b>FALSE</b>, and FaxDevReportStatus() should return any of the following codes: FS_LINE_UNAVAILABLE, FS_NO_ANSWER, FS_NO_DIAL_TONE, FS_DISCONNECTED, FS_BUSY, FS_NOT_FAX_CALL, or FS_FATAL_ERROR. If after a failed fax the fax should not be re-sent, FaxDevReportStatus() should return any code other than those listed here.</div>
<div> </div>

## -remarks

The FSP must respond to the <b>FaxDevSend</b> function by making the call, sending the data, and terminating the call. The provider can call the <a href="/windows/desktop/api/tapi/nf-tapi-linesetmediamode">lineSetMediaMode</a> function to correctly set the call's media mode. The fax service provider must dial the number specified by the <b>ReceiverNumber</b> member of the <a href="/windows/desktop/api/faxdev/ns-faxdev-fax_send">FAX_SEND</a> structure. 
        

The FSP has ownership of the line while in the context of the <b>FaxDevSend</b> function, and it must handle all protocol and error correction. 
        

The data stream stored in the file specified by the <b>FileName</b> member of the <a href="/windows/desktop/api/faxdev/ns-faxdev-fax_send">FAX_SEND</a> structure is a Tagged Image File Format Class F (TIFF Class F) file. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-fax-image-format">Fax Image Format</a>. 
        

To notify the fax service that a call has been established, the FSP must call the <a href="/previous-versions/windows/desktop/api/faxdev/nc-faxdev-pfax_send_callback">FaxSendCallback</a> function pointed to by the <i>FaxSendCallback</i> parameter. The callback function also provides the fax service with the call handle that TAPI assigns. This handle is necessary for TAPI message routing. If the FSP does not call <i>FaxSendCallback</i>, it will miss all call-specific events for the send operation.

## -see-also

<a href="/windows/desktop/api/faxdev/ns-faxdev-fax_send">FAX_SEND</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-provider-functions">Fax Service Provider Functions</a>



<a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevreceive">FaxDevReceive</a>



<a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevstartjob">FaxDevStartJob</a>



<a href="/previous-versions/windows/desktop/api/faxdev/nc-faxdev-pfax_send_callback">FaxSendCallback</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-using-the-fax-service-provider-api">Using the Fax Service Provider API</a>