---
UID: NF:certenroll.IX509PrivateKey.put_Silent
title: IX509PrivateKey::put_Silent (certenroll.h)
description: Specifies or retrieves a Boolean value that indicates whether the Certificate Enrollment Control is allowed to display a dialog box when the private key is accessed. (Put)
helpviewer_keywords: ["IX509PrivateKey interface [Security]","Silent property","IX509PrivateKey.Silent","IX509PrivateKey.put_Silent","IX509PrivateKey::Silent","IX509PrivateKey::get_Silent","IX509PrivateKey::put_Silent","Silent property [Security]","Silent property [Security]","IX509PrivateKey interface","certenroll/IX509PrivateKey::Silent","certenroll/IX509PrivateKey::get_Silent","certenroll/IX509PrivateKey::put_Silent","put_Silent","security.ix509privatekey_silent_property"]
old-location: security\ix509privatekey_silent_property.htm
tech.root: security
ms.assetid: 4f61a513-620c-48c4-b9dd-032b13a9f654
ms.date: 12/05/2018
ms.keywords: IX509PrivateKey interface [Security],Silent property, IX509PrivateKey.Silent, IX509PrivateKey.put_Silent, IX509PrivateKey::Silent, IX509PrivateKey::get_Silent, IX509PrivateKey::put_Silent, Silent property [Security], Silent property [Security],IX509PrivateKey interface, certenroll/IX509PrivateKey::Silent, certenroll/IX509PrivateKey::get_Silent, certenroll/IX509PrivateKey::put_Silent, put_Silent, security.ix509privatekey_silent_property
req.header: certenroll.h
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
req.dll: CertEnroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509PrivateKey::put_Silent
 - certenroll/IX509PrivateKey::put_Silent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509PrivateKey.Silent
 - IX509PrivateKey.get_Silent
 - IX509PrivateKey.put_Silent
---

# IX509PrivateKey::put_Silent


## -description

The <b>Silent</b> property specifies or retrieves a Boolean value that indicates whether the Certificate Enrollment Control is allowed to display  a dialog box when the private key is accessed.

This property is read/write.

## -parameters

## -remarks

If the user interface is not allowed but is required to access the private key, operations that require the user interface will fail.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a>
