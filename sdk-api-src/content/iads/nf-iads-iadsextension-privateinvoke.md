---
UID: NF:iads.IADsExtension.PrivateInvoke
title: IADsExtension::PrivateInvoke (iads.h)
description: The IADsExtension::PrivateInvoke method is normally called by ADSI after the IADsExtension::PrivateGetIDsOfNames method. This method can either have a custom implementation or it can delegate the operation to IDispatch::DispInvoke method.
helpviewer_keywords: ["DISPATCH_METHOD","DISPATCH_PROPERTYGET","DISPATCH_PROPERTYPUT","DISPATCH_PROPERTYPUTREF","IADsExtension interface [ADSI]","PrivateInvoke method","IADsExtension.PrivateInvoke","IADsExtension::PrivateInvoke","PrivateInvoke","PrivateInvoke method [ADSI]","PrivateInvoke method [ADSI]","IADsExtension interface","_ds_iadsextension_privateinvoke","adsi.iadsextension__privateinvoke","adsi.iadsextension_privateinvoke","iads/IADsExtension::PrivateInvoke"]
old-location: adsi\iadsextension_privateinvoke.htm
tech.root: adsi
ms.assetid: 5af74a05-df64-4679-890b-a5a031633fd8
ms.date: 12/05/2018
ms.keywords: DISPATCH_METHOD, DISPATCH_PROPERTYGET, DISPATCH_PROPERTYPUT, DISPATCH_PROPERTYPUTREF, IADsExtension interface [ADSI],PrivateInvoke method, IADsExtension.PrivateInvoke, IADsExtension::PrivateInvoke, PrivateInvoke, PrivateInvoke method [ADSI], PrivateInvoke method [ADSI],IADsExtension interface, _ds_iadsextension_privateinvoke, adsi.iadsextension__privateinvoke, adsi.iadsextension_privateinvoke, iads/IADsExtension::PrivateInvoke
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
 - IADsExtension::PrivateInvoke
 - iads/IADsExtension::PrivateInvoke
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
 - IADsExtension.PrivateInvoke
---

# IADsExtension::PrivateInvoke


## -description

The <b>IADsExtension::PrivateInvoke</b> method is normally called by ADSI after the  <a href="/windows/desktop/api/iads/nf-iads-iadsextension-privategetidsofnames">IADsExtension::PrivateGetIDsOfNames</a> method. This method can either have a custom implementation or it can delegate the operation to <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispinvoke">IDispatch::DispInvoke</a> method.

## -parameters

### -param dispidMember [in]

Identifies the member. Use the <a href="/windows/desktop/api/iads/nf-iads-iadsextension-privategetidsofnames">IADsExtension::PrivateGetIDsOfNames</a> method to obtain the dispatch identifier.

### -param riid [in]

Reserved for future use. Must be IID_NULL.

### -param lcid [in]

The locale context in which to interpret arguments. The <a href="/windows/desktop/api/iads/nf-iads-iadsextension-privategetidsofnames">IADsExtension::PrivateGetIDsOfNames</a> function uses <i>lcid</i>. It is also passed to the <b>PrivateInvoke</b> method to allow the object to interpret the arguments that are specific to a locale.

### -param wFlags [in]

Flags that describe the context of the <b>PrivateInvoke</b> call, include.



#### DISPATCH_METHOD

The member is invoked as a method. If a property has the same name, both this and the <b>DISPATCH_PROPERTYGET</b> flag may be set.



#### DISPATCH_PROPERTYGET

The member is retrieved as a property or data member.



#### DISPATCH_PROPERTYPUT

The member is changed as a property or data member.



#### DISPATCH_PROPERTYPUTREF

The member is changed by a reference assignment, rather than a value assignment. This flag is valid only when the property accepts a reference to an object.

### -param pdispparams [in]

Pointer to a <a href="/windows/desktop/api/oaidl/ns-oaidl-dispparams">DISPPARAMS</a> structure that receives an array of arguments, an array of argument DISPIDs for named arguments, and counts for the number of elements in the arrays.

### -param pvarResult [out]

Pointer to the location where the result is to be stored, or <b>NULL</b> if the caller expects no result. This argument is ignored if <b>DISPATCH_PROPERTYPUT</b> or <b>DISPATCH_PROPERTYPUTREF</b> is specified.

### -param pexcepinfo [out]

Pointer to a structure that contains exception data. This structure should be filled in if <b>DISP_E_EXCEPTION</b> is returned. Can be <b>NULL</b>.

### -param puArgErr [out]

The index within the <b>rgvarg</b> member of the <a href="/windows/desktop/api/oaidl/ns-oaidl-dispparams">DISPPARAMS</a> structure in <i>pdispparams</i> for the first argument that has an error. Arguments are stored in the <b>rgvarg</b> array in reverse order, so the first argument is the one with the highest index in the array. This parameter is returned only when the resulting return value is <b>DISP_E_TYPEMISMATCH</b> or <b>DISP_E_PARAMNOTFOUND</b>.

## -returns

This method supports the standard return values, as well as the following.

For more information about other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispinvoke">DispInvoke</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsextension">IADsExtension</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsextension-privategetidsofnames">IADsExtension::PrivateGetIDsOfNames</a>