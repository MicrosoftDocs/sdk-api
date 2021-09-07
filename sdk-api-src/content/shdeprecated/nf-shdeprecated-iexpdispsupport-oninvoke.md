---
UID: NF:shdeprecated.IExpDispSupport.OnInvoke
title: IExpDispSupport::OnInvoke (shdeprecated.h)
description: Deprecated. Gets ambient properties.
helpviewer_keywords: ["DISPATCH_METHOD","DISPATCH_PROPERTYGET","DISPATCH_PROPERTYPUT","DISPATCH_PROPERTYPUTREF","IExpDispSupport interface [Windows Shell]","OnInvoke method","IExpDispSupport.OnInvoke","IExpDispSupport::OnInvoke","OnInvoke","OnInvoke method [Windows Shell]","OnInvoke method [Windows Shell]","IExpDispSupport interface","shdeprecated/IExpDispSupport::OnInvoke","shell.IExpDispSupport_OnInvoke","zone_IExpDispSupport_OnInvoke"]
old-location: shell\IExpDispSupport_OnInvoke.htm
tech.root: shell
ms.assetid: 92228340-2472-4920-90b7-ce46cab7406e
ms.date: 12/05/2018
ms.keywords: DISPATCH_METHOD, DISPATCH_PROPERTYGET, DISPATCH_PROPERTYPUT, DISPATCH_PROPERTYPUTREF, IExpDispSupport interface [Windows Shell],OnInvoke method, IExpDispSupport.OnInvoke, IExpDispSupport::OnInvoke, OnInvoke, OnInvoke method [Windows Shell], OnInvoke method [Windows Shell],IExpDispSupport interface, shdeprecated/IExpDispSupport::OnInvoke, shell.IExpDispSupport_OnInvoke, zone_IExpDispSupport_OnInvoke
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
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
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - IExpDispSupport::OnInvoke
 - shdeprecated/IExpDispSupport::OnInvoke
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IExpDispSupport.OnInvoke
---

# IExpDispSupport::OnInvoke


## -description

Deprecated. Gets ambient properties.

## -parameters

### -param dispidMember [in]

Type: <b>DISPID</b>

A dispatch ID that identifies the member being invoked.

### -param iid [in]

Type: <b>REFIID</b>

Reserved. Must be IID_NULL.

### -param lcid [in]

Type: <b>LCID</b>

A locale ID providing a locale context in which to interpret arguments. Applications that do not support multiple languages can ignore this parameter.

### -param wFlags [in]

Type: <b>WORD</b>

Flags describing the context of the call, including the following.



#### DISPATCH_METHOD

The member is invoked as a method. If a property has the same name, both this and the DISPATCH_PROPERTYGET flag may be set. The member is invoked as a method. If a property has the same name, both this and the DISPATCH_PROPERTYGET flag may be set.



#### DISPATCH_PROPERTYGET

The member is retrieved as a property or data member.



#### DISPATCH_PROPERTYPUT

The member is changed as a property or data member.



#### DISPATCH_PROPERTYPUTREF

The member is changed by a reference assignment, rather than a value assignment. This flag is valid only when the property accepts a reference to an object.

### -param pdispparams

Type: <b><a href="/windows/desktop/api/oaidl/ns-oaidl-dispparams">DISPPARAMS</a>*</b>

A pointer to a <a href="/windows/desktop/api/oaidl/ns-oaidl-dispparams">DISPPARAMS</a> structure containing an array of arguments, an array of argument DISPIDs for named arguments, and counts for the number of elements in the arrays.

### -param pVarResult

Type: <b>VARIANT*</b>

A pointer to the location where the result is to be stored, or <b>NULL</b> if the caller expects no result. This argument is ignored if DISPATCH_PROPERTYPUT or DISPATCH_PROPERTYPUTREF is specified.

### -param pexcepinfo

Type: <b>EXCEPINFO*</b>

A pointer to a structure that contains exception information. This structure should be filled in if DISP_E_EXCEPTION is returned. Can be <b>NULL</b>.

### -param puArgErr

Type: <b>UINT*</b>

The index within the <b>rgvarg</b> member of the <a href="/windows/desktop/api/oaidl/ns-oaidl-dispparams">DISPPARAMS</a> structure of the first argument that has an error. Arguments are stored in <b>rgvarg</b> in reverse order, so the first argument is the one with the highest index in the array. This parameter is returned only when the resulting return value is DISP_E_TYPEMISMATCH or DISP_E_PARAMNOTFOUND. This argument can be set to <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For more information, see <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke">IDispatch::Invoke</a>.