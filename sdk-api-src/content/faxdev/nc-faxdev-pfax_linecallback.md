---
UID: NC:faxdev.PFAX_LINECALLBACK
title: PFAX_LINECALLBACK
author: windows-sdk-content
description: The FaxLineCallback function is an application-defined or library-defined callback function that the fax service calls to deliver Telephony Application Programming Interface (TAPI) events to the fax service provider (FSP).
old-location: fax\_mfax_faxlinecallback.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxfspapiref_8xpn.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: FaxLineCallback, FaxLineCallback callback function [Fax Service], PFAX_LINECALLBACK, PFAX_LINECALLBACK callback, _mfax_faxlinecallback, fax._mfax_faxlinecallback, faxdev/FaxLineCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: faxdev.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - FaxDev.h
api_name:
 - FaxLineCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# PFAX_LINECALLBACK callback function


## -description


The <i>FaxLineCallback</i> function is an application-defined or library-defined callback function that the fax service calls to deliver Telephony Application Programming Interface (TAPI) events to the fax service provider (FSP).

The <b>PFAX_LINECALLBACK</b> data type is a pointer to a <i>FaxLineCallback</i> function. <i>FaxLineCallback</i> is a placeholder for an application-defined or library-defined function name.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax handle returned by the <a href="https://msdn.microsoft.com/en-us/library/ms684541(v=VS.85).aspx">FaxDevStartJob</a> function.


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

Specifies a parameter for the message. For information about parameter values passed in this structure, see <a href="https://msdn.microsoft.com/dc11134e-6c20-426e-834e-508bf855e5da">Line Device Messages</a> in the TAPI documentation.


### -param dwParam2 [in]

Type: <b>DWORD_PTR</b>

Specifies a parameter for the message.


### -param dwParam3 [in]

Type: <b>DWORD_PTR</b>

Specifies a parameter for the message.


## -returns



This callback function does not return a value.




## -remarks



The FSP must register the <i>FaxLineCallback</i> callback function by passing its address when the fax service calls the <a href="https://msdn.microsoft.com/en-us/library/ms684545(v=VS.85).aspx">FaxDevInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms684546(v=VS.85).aspx">Fax Service Provider Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684545(v=VS.85).aspx">FaxDevInitialize</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684541(v=VS.85).aspx">FaxDevStartJob</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693428(v=VS.85).aspx">Using the Fax Service Provider API</a>



<a href="https://msdn.microsoft.com/en-us/library/ms735983(v=VS.85).aspx">lineInitializeEx</a>
 

 

