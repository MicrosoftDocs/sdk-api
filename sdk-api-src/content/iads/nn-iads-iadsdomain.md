---
UID: NN:iads.IADsDomain
title: IADsDomain (iads.h)
description: The IADsDomain interface is a dual interface that inherits from IADs.
helpviewer_keywords: ["IADsDomain","IADsDomain interface [ADSI]","IADsDomain interface [ADSI]","described","_ds_iadsdomain","adsi.iadsdomain","iads/IADsDomain"]
old-location: adsi\iadsdomain.htm
tech.root: adsi
ms.assetid: 9d4b1e9c-93b1-4aee-b20d-a7693fd0a61b
ms.date: 12/05/2018
ms.keywords: IADsDomain, IADsDomain interface [ADSI], IADsDomain interface [ADSI],described, _ds_iadsdomain, adsi.iadsdomain, iads/IADsDomain
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
 - IADsDomain
 - iads/IADsDomain
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
 - IADsDomain
---

# IADsDomain interface


## -description

The <b>IADsDomain</b> interface is a dual interface that inherits from  <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. It is designed to represent a network domain and manage domain accounts. Use this interface to determine whether the domain is actually a Workgroup, to specify how frequently a user must change a password, and to specify the maximum number of invalid password logins allowed before a lockout on the account is set. To change a password, call the <b>ChangePassword</b> method on an ADSI object that supports password controls. For example, to change the password of a user account, call  <a href="/windows/desktop/api/iads/nf-iads-iadsuser-changepassword">IADsUser::ChangePassword</a> on the user object.

## -inheritance

The <b>IADsDomain</b> interface inherits from <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> and <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. <b>IADsDomain</b> also has these types of members:

## -remarks

For the WinNT provider supplied by Microsoft, this interface is implemented on the <b>WinNTDomain</b> object.

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="/windows/desktop/ADSI/iadsdomain-property-methods">IADsDomain Property
    Methods</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsuser-setpassword">IADsUser::SetPassword</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
