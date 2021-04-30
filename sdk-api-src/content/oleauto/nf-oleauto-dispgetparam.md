---
UID: NF:oleauto.DispGetParam
title: DispGetParam function (oleauto.h)
description: Retrieves a parameter from the DISPPARAMS structure, checking both named parameters and positional parameters, and coerces the parameter to the specified type.
helpviewer_keywords: ["DispGetParam","DispGetParam function [Automation]","_oa96_DispGetParam","automat.dispgetparam","oleauto/DispGetParam"]
old-location: automat\dispgetparam.htm
tech.root: automat
ms.assetid: 72cdb768-4791-4606-8e5d-72cd003e854a
ms.date: 12/05/2018
ms.keywords: DispGetParam, DispGetParam function [Automation], _oa96_DispGetParam, automat.dispgetparam, oleauto/DispGetParam
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DispGetParam
 - oleauto/DispGetParam
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - DispGetParam
---

# DispGetParam function


## -description

Retrieves a parameter from the DISPPARAMS structure, checking both named parameters and positional parameters, and coerces the parameter to the specified type.

## -parameters

### -param pdispparams [in]

The parameters passed to <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke">Invoke</a>.

### -param position

The position of the parameter in the parameter list. <b>DispGetParam</b> starts at the end of the array, so if position is 0, the last parameter in the array is returned.

### -param vtTarg

The type the argument should be coerced to.

### -param pvarResult [out]

the variant to pass the parameter into.

### -param puArgErr [out, optional]

On return, the index of the argument that caused a DISP_E_TYPEMISMATCH error. This pointer is returned to <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke">Invoke</a> to indicate the position of the argument in DISPPARAMS that caused the error.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_BADVARTYPE</b></dt>
</dl>
</td>
<td width="60%">
The variant type <i>vtTarg</i> is not supported.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
The retrieved parameter could not be coerced to the specified type.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_PARAMNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The parameter indicated by <i>position</i> could not be found.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_TYPEMISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The argument could not be coerced to the specified type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG
</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY
</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>

## -remarks

The output parameter <i>pvarResult</i> must be a valid variant. Any existing contents are released in the standard way. The contents of the variant are freed with <b>VariantFree</b>.

If you have used <b>DispGetParam</b> to get the right side of a property put operation, the second parameter should be DISPID_PROPERTYPUT. For example:


```cpp
DispGetParam(&dispparams, DISPID_PROPERTYPUT, VT_BOOL, &varResult, &uiArg)
```


Named parameters cannot be accessed positionally, and vice versa.


#### Examples

The following example uses <b>DispGetParam</b> to set X and Y properties.


```cpp
STDMETHODIMP
CPoint::Invoke(
   DISPID dispidMember,
   REFIID riid,
   LCID lcid,
   unsigned short wFlags,
   DISPPARAMS * pdispparams,
   VARIANT * pvarResult,
   EXCEPINFO * pExcepInfo,
   unsigned int * puArgErr)
{
   unsigned int uArgErr;
   HRESULT hresult;
   VARIANTARG varg0;
   VARIANT varResultDummy;

   // Make sure the wFlags are valid.
   if(wFlags & ~(DISPATCH_METHOD | DISPATCH_PROPERTYGET |
      DISPATCH_PROPERTYPUT | DISPATCH_PROPERTYPUTREF))
      return E_INVALIDARG;

   // This object only exposes a "default" interface.
   if(!IsEqualIID(riid, IID_NULL))
      return DISP_E_UNKNOWNINTERFACE;

   // It simplifies the following code if the caller
   // ignores the return value.
   if(puArgErr == NULL)
      puArgErr = &uArgErr;
   if(pvarResult == NULL)
      pvarResult = &varResultDummy;

   VariantInit(&varg0);

   // Assume the return type is void, unless otherwise is found.
   VariantInit(pvarResult);

   switch(dispidMember){
   case IDMEMBER_CPOINT_GETX:
      V_VT(pvarResult) = VT_I2;
      V_I2(pvarResult) = GetX();
      break;

   case IDMEMBER_CPOINT_SETX:
      hresult = DispGetParam(pdispparams, 0, VT_I2, &varg0, puArgErr);
      if(hresult != NOERROR)
         return hresult;
      SetX(V_I2(&varg0));
      break;

   case IDMEMBER_CPOINT_GETY:
      V_VT(pvarResult) = VT_I2;
      V_I2(pvarResult) = GetY();
      break;

   case IDMEMBER_CPOINT_SETY:
      hresult = DispGetParam(pdispparams, 0, VT_I2, &varg0, puArgErr);
      if(hresult != NOERROR)
         return hresult;
      SetY(V_I2(&varg0));
      break;

   default:
      return DISP_E_MEMBERNOTFOUND;
   }
   return NOERROR;
}
```

## -see-also

<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createstddispatch">CreateStdDispatch</a>



<a href="/previous-versions/windows/desktop/automat/dispatch-functions">Creation of Dispatch API Functions</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke">IDispatch::Invoke</a>