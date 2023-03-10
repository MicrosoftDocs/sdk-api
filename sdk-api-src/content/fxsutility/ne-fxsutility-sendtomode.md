---
UID: NE:fxsutility.SendToMode
title: SendToMode (fxsutility.h)
description: Defines the way a file will be faxed from within an application. With Windows Vista there is only one possible value.
helpviewer_keywords: ["SEND_TO_FAX_RECIPIENT_ATTACHMENT","SendToMode","SendToMode enumeration [Fax Service]","_mfax_sendtomode","fax._mfax_sendtomode","fxsutility/SEND_TO_FAX_RECIPIENT_ATTACHMENT","fxsutility/SendToMode"]
old-location: fax\_mfax_sendtomode.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\shellextension\e\faxinto_z_sendtomode.htm
ms.date: 12/05/2018
ms.keywords: SEND_TO_FAX_RECIPIENT_ATTACHMENT, SendToMode, SendToMode enumeration [Fax Service], _mfax_sendtomode, fax._mfax_sendtomode, fxsutility/SEND_TO_FAX_RECIPIENT_ATTACHMENT, fxsutility/SendToMode
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SendToMode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SendToMode
 - fxsutility/SendToMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fxsutility.h
api_name:
 - SendToMode
---

# SendToMode enumeration


## -description

Defines the way a file will be faxed from within an application. With Windows Vista there is only one possible value.

## -enum-fields

### -field SEND_TO_FAX_RECIPIENT_ATTACHMENT

The file is faxed as it is. The user cannot add typed material preceding it or following it.

## -remarks

This enumeration is used primarily as a parameter for the <a href="/previous-versions/windows/desktop/api/fxsutility/nf-fxsutility-sendtofaxrecipient">SendToFaxRecipient</a> function.

## -see-also

<a href="/previous-versions/windows/desktop/api/fxsutility/nf-fxsutility-sendtofaxrecipient">SendToFaxRecipient</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-shell-fax-extension-functions">Shell Fax Extension Functions</a>

