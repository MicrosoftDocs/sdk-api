---
UID: NC:faxdev.PFAX_LINECALLBACK
title: PFAX_LINECALLBACK (faxdev.h)
description: The FaxLineCallback function is an application-defined or library-defined callback function that the fax service calls to deliver Telephony Application Programming Interface (TAPI) events to the fax service provider (FSP).
helpviewer_keywords: ["FaxLineCallback","FaxLineCallback callback function [Fax Service]","PFAX_LINECALLBACK","PFAX_LINECALLBACK callback","_mfax_faxlinecallback","fax._mfax_faxlinecallback","faxdev/FaxLineCallback"]
old-location: fax\_mfax_faxlinecallback.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxfspapiref_8xpn.htm
ms.date: 12/05/2018
ms.keywords: FaxLineCallback, FaxLineCallback callback function [Fax Service], PFAX_LINECALLBACK, PFAX_LINECALLBACK callback, _mfax_faxlinecallback, fax._mfax_faxlinecallback, faxdev/FaxLineCallback
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
 - PFAX_LINECALLBACK
 - faxdev/PFAX_LINECALLBACK
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
 - FaxLineCallback
---

# PFAX_LINECALLBACK callback function


## -description

The <i>FaxLineCallback</i> function is an application-defined or library-defined callback function that the fax service calls to deliver Telephony Application Programming Interface (TAPI) events to the fax service provider (FSP).

The <b>PFAX_LINECALLBACK</b> data type is a pointer to a <i>FaxLineCallback</i> function. <i>FaxLineCallback</i> is a placeholder for an application-defined or library-defined function name.

## -parameters

### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax handle returned by the <a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevstartjob">FaxDevStartJob</a> function.

### -param hDevice [in]

Type: <b>DWORD</b>

Specifies a handle to either a line device or a call device. To determine whether this handle is a line handle or a call handle, use the context that the <i>dwMessage</i> parameter provides.

### -param dwMessage [in]

Type: <b>DWORD</b>

Specifies a line device or a call device message.

### -param dwInstance

Type: <b>DWORD_PTR</b>

Reserved; should not be used by the FSP.

### -param dwParam1 [in]

Type: <b>DWORD_PTR</b>

Specifies a parameter for the message. For information about parameter values passed in this structure, see <a href="/windows/desktop/Tapi/line-device-messages">Line Device Messages</a> in the TAPI documentation.

### -param dwParam2 [in]

Type: <b>DWORD_PTR</b>

Specifies a parameter for the message.

### -param dwParam3 [in]

Type: <b>DWORD_PTR</b>

Specifies a parameter for the message.

## -remarks

The FSP must register the <i>FaxLineCallback</i> callback function by passing its address when the fax service calls the <a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevinitialize">FaxDevInitialize</a> function.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-provider-functions">Fax Service Provider Functions</a>



<a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevinitialize">FaxDevInitialize</a>



<a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevstartjob">FaxDevStartJob</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-using-the-fax-service-provider-api">Using the Fax Service Provider API</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a>