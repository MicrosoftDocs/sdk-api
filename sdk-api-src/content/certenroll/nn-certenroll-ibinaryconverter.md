---
UID: NN:certenroll.IBinaryConverter
title: IBinaryConverter (certenroll.h)
description: Contains general methods that enable you to create a Unicode-encoded string from a byte array, create a byte array from a Unicode-encoded string, and modify the type of Unicode encoding applied to a string.
helpviewer_keywords: ["IBinaryConverter","IBinaryConverter interface [Security]","IBinaryConverter interface [Security]","described","certenroll/IBinaryConverter","security.ibinaryconverter"]
old-location: security\ibinaryconverter.htm
tech.root: security
ms.assetid: 495a321a-3005-4537-b082-5003e437d21f
ms.date: 12/05/2018
ms.keywords: IBinaryConverter, IBinaryConverter interface [Security], IBinaryConverter interface [Security],described, certenroll/IBinaryConverter, security.ibinaryconverter
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
 - IBinaryConverter
 - certenroll/IBinaryConverter
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
 - IBinaryConverter
---

# IBinaryConverter interface


## -description

The <b>IBinaryConverter</b> interface contains general methods that enable you to create a Unicode-encoded string from a byte array, create a byte array from a Unicode-encoded string, and modify the type of Unicode encoding applied to  a string. You can use this interface to represent a <a href="/windows/desktop/SecGloss/c-gly">certificate BLOB</a> as a printable string or to decode the string back into a certificate BLOB.

## -inheritance

The <b>IBinaryConverter</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IBinaryConverter</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
