---
UID: NF:fxsutility.CanSendToFaxRecipient
title: CanSendToFaxRecipient function (fxsutility.h)
description: Called by an application to determine whether to make a menu item or other UI available that calls the Windows Vista function SendToFaxRecipient.
helpviewer_keywords: ["CanSendToFaxRecipient","CanSendToFaxRecipient function [Fax Service]","_mfax_cansendtofaxrecipient","fax._mfax_cansendtofaxrecipient","fxsutility/CanSendToFaxRecipient"]
old-location: fax\_mfax_cansendtofaxrecipient.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\shellextension\f\faxshell_cansendtofaxrecipient.htm
ms.date: 12/05/2018
ms.keywords: CanSendToFaxRecipient, CanSendToFaxRecipient function [Fax Service], _mfax_cansendtofaxrecipient, fax._mfax_cansendtofaxrecipient, fxsutility/CanSendToFaxRecipient
req.header: fxsutility.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: fxsutility.lib
req.dll: Fxsutility.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CanSendToFaxRecipient
 - fxsutility/CanSendToFaxRecipient
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fxsutility.dll
api_name:
 - CanSendToFaxRecipient
---

# CanSendToFaxRecipient function


## -description

Called by an application to determine whether to make a menu item or other UI available that calls the Windows Vista function <a href="/previous-versions/windows/desktop/api/fxsutility/nf-fxsutility-sendtofaxrecipient">SendToFaxRecipient</a>.



## -returns

Type: <b>BOOL</b>

<b>TRUE</b>, if the following conditions are met; otherwise <b>FALSE</b>. 
                <ul>
<li>The operating system is Windows Vista or later.</li>
<li>The fax service is installed.</li>
<li>The current user has a fax account setup with the fax service.</li>
</ul>

## -remarks

Typically, this function is called when the application launches.

## -see-also

<a href="/previous-versions/windows/desktop/api/fxsutility/nf-fxsutility-sendtofaxrecipient">SendToFaxRecipient</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-shell-fax-extension-functions">Shell Fax Extension Functions</a>
