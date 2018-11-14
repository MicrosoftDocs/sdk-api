---
UID: NC:cryptdlg.PFNCMHOOKPROC
title: PFNCMHOOKPROC
author: windows-sdk-content
description: Called before messages are processed by the certificate selection dialog box produced by the CertSelectCertificate function.
old-location: security\pfncmhookproc.htm
tech.root: seccrypto
ms.assetid: 7172c995-a46b-437b-beaf-a0649cb8ec3d
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: PFNCMHOOKPROC, PFNCMHOOKPROC callback, PFNCMHOOKPROC callback function [Security], cryptdlg/PFNCMHOOKPROC, security.pfncmhookproc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: cryptdlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - CryptDlg.h
api_name:
 - PFNCMHOOKPROC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFNCMHOOKPROC callback function


## -description


The <b>PFNCMHOOKPROC</b> function is a hook procedure that is called before messages are processed by the certificate selection dialog box produced by the <a href="https://msdn.microsoft.com/8160ea08-c7c0-40f5-8771-6603f768744b">CertSelectCertificate</a> function. The function allows the caller to customize the dialog box. <b>PFNCMHOOKPROC</b> is an application-defined callback function specified in the <a href="https://msdn.microsoft.com/49184872-d636-4e55-8e32-0f38b49b5c21">CERT_SELECT_STRUCT</a> structure. The <b>CERT_SELECT_STRUCT</b> structure is a parameter in the <a href="https://msdn.microsoft.com/8160ea08-c7c0-40f5-8771-6603f768744b">CertSelectCertificate</a> function. The <b>PFNCMHOOKPROC</b> function must be implemented by the developer to suit each application.


## -parameters




### -param hwndDialog [in]

A handle to a dialog box window.


### -param message [in]

The message.


### -param wParam [in]

Additional information about the message sent or posted.


### -param lParam [in]

 Additional information about the message sent or posted.


## -returns



Return a nonzero value (<b>TRUE</b>) if this function processes the message. Return zero (<b>FALSE</b>) if this function does not process the message.




## -remarks



For information about hooks, see <a href="_win32_hooks_cpp">Hooks</a>.




## -see-also




<a href="https://msdn.microsoft.com/49184872-d636-4e55-8e32-0f38b49b5c21">CERT_SELECT_STRUCT</a>



<a href="https://msdn.microsoft.com/8160ea08-c7c0-40f5-8771-6603f768744b">CertSelectCertificate</a>
 

 

