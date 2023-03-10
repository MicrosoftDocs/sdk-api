---
UID: NN:iads.IADsComputer
title: IADsComputer (iads.h)
description: The IADsComputer interface is a dual interface that inherits from IADs.
helpviewer_keywords: ["IADsComputer","IADsComputer interface [ADSI]","IADsComputer interface [ADSI]","described","_ds_iadscomputer","adsi.iadscomputer","iads/IADsComputer"]
old-location: adsi\iadscomputer.htm
tech.root: adsi
ms.assetid: e2b90a98-5777-42c2-95dd-4623e738c4da
ms.date: 12/05/2018
ms.keywords: IADsComputer, IADsComputer interface [ADSI], IADsComputer interface [ADSI],described, _ds_iadscomputer, adsi.iadscomputer, iads/IADsComputer
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Activeds.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsComputer
 - iads/IADsComputer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsComputer
---

# IADsComputer interface


## -description

The <b>IADsComputer</b> interface is a dual interface that inherits from  <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. It is designed to represent and manage a computer, such as a server, client, workstation, and so on, on a network. You can manipulate the properties of this interface to access data about a computer. The data includes the operating system, the make and model, processor, computer identifier, its network addresses, and so on.
  
<div class="alert"><b>Note</b>  The <b>IADsComputer</b> interface is not implemented by the LDAP ADSI provider. For more information, see <a href="/windows/desktop/ADSI/adsi-objects-of-ldap">ADSI Objects of LDAP</a>.</div><div> </div>

## -inheritance

The <b>IADsComputer</b> interface inherits from <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> and <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. <b>IADsComputer</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="/windows/desktop/ADSI/iadscomputer-property-methods">IADsComputer Property
    Methods</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
