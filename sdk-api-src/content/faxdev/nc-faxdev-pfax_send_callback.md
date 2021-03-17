---
UID: NC:faxdev.PFAX_SEND_CALLBACK
title: PFAX_SEND_CALLBACK (faxdev.h)
description: The FaxSendCallback function is an application-defined or library-defined callback function that a fax service provider (FSP) calls to notify the fax service that an outgoing fax call is in progress.
helpviewer_keywords: ["FaxSendCallback","FaxSendCallback callback function [Fax Service]","PFAX_SEND_CALLBACK","PFAX_SEND_CALLBACK callback","_mfax_faxsendcallback","fax._mfax_faxsendcallback","faxdev/FaxSendCallback"]
old-location: fax\_mfax_faxsendcallback.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxfspapiref_8xt7.htm
ms.date: 12/05/2018
ms.keywords: FaxSendCallback, FaxSendCallback callback function [Fax Service], PFAX_SEND_CALLBACK, PFAX_SEND_CALLBACK callback, _mfax_faxsendcallback, fax._mfax_faxsendcallback, faxdev/FaxSendCallback
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
 - PFAX_SEND_CALLBACK
 - faxdev/PFAX_SEND_CALLBACK
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
 - FaxSendCallback
---

# PFAX_SEND_CALLBACK callback function


## -description

The <i>FaxSendCallback</i> function is an application-defined or library-defined callback function that a fax service provider (FSP) calls to notify the fax service that an outgoing fax call is in progress.

The <b>PFAX_SEND_CALLBACK</b> data type is a pointer to a <i>FaxSendCallback</i> function. <i>FaxSendCallback</i> is a placeholder for an application-defined or library-defined function name.

## -parameters

### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax handle returned by the <a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevstartjob">FaxDevStartJob</a> function.

### -param CallHandle [in]

Type: <b>HCALL</b>

Specifies a call handle returned by the TAPI 2.x <a href="/windows/desktop/Tapi/line-callstate">LINE_CALLSTATE</a> message.

### -param Reserved1 [in]

Type: <b>DWORD</b>

This parameter is reserved for future use by Microsoft. It must be set to zero.

### -param Reserved2 [in]

Type: <b>DWORD</b>

This parameter is reserved for future use by Microsoft. It must be set to zero.

## -returns

Type: <b>BOOL</b>

The fax service returns a value of <b>TRUE</b> to indicate that the active fax operation should continue.

The fax service returns a value of <b>FALSE</b> to indicate that the active fax operation should be terminated. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <i>FaxSendCallback</i> callback function provides the fax service with the <i>CallHandle</i> that TAPI assigns. This handle is necessary for TAPI message routing. If the FSP does not call <i>FaxSendCallback</i>, it will miss all further call events.

A virtual FSP does not need the <i>FaxSendCallback</i> function.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-provider-functions">Fax Service Provider Functions</a>



<a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevsend">FaxDevSend</a>



<a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevstartjob">FaxDevStartJob</a>



<a href="/windows/desktop/Tapi/line-callstate">LINE_CALLSTATE</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-using-the-fax-service-provider-api">Using the Fax Service Provider API</a>