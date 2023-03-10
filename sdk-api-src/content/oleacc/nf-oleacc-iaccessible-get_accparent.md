---
UID: NF:oleacc.IAccessible.get_accParent
title: IAccessible::get_accParent (oleacc.h)
description: The IAccessible::get_accParent method retrieves the IDispatch of the object's parent. All objects support this property.
helpviewer_keywords: ["IAccessible interface [Windows Accessibility]","get_accParent method","IAccessible.get_accParent","IAccessible::get_accParent","_msaa_IAccessible_get_accParent","get_accParent","get_accParent method [Windows Accessibility]","get_accParent method [Windows Accessibility]","IAccessible interface","msaa.iaccessible_iaccessible__get_accparent","oleacc/IAccessible::get_accParent","winauto.iaccessible_iaccessible__get_accparent"]
old-location: winauto\iaccessible_iaccessible__get_accparent.htm
tech.root: WinAuto
ms.assetid: 7c8c5208-ea77-47b2-913d-314ade0313f5
ms.date: 12/05/2018
ms.keywords: IAccessible interface [Windows Accessibility],get_accParent method, IAccessible.get_accParent, IAccessible::get_accParent, _msaa_IAccessible_get_accParent, get_accParent, get_accParent method [Windows Accessibility], get_accParent method [Windows Accessibility],IAccessible interface, msaa.iaccessible_iaccessible__get_accparent, oleacc/IAccessible::get_accParent, winauto.iaccessible_iaccessible__get_accparent
req.header: oleacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Oleacc.lib
req.dll: Oleacc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95
ms.custom: 19H1
f1_keywords:
 - IAccessible::get_accParent
 - oleacc/IAccessible::get_accParent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Oleacc.dll
api_name:
 - IAccessible.get_accParent
---

# IAccessible::get_accParent


## -description

The <b>IAccessible::get_accParent</b> method retrieves the <a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a> of the object's parent. All objects support this property.

## -parameters

### -param ppdispParent [out, retval]

Type: <b>IDispatch**</b>

 Receives the address of the parent object's <a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a> interface. If no parent exists or if the child cannot access its parent, the variable is set to <b>NULL</b>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK.

If not successful, returns one of the values in the table that follows, or another standard <a href="/windows/desktop/WinAuto/return-values">COM error code</a>. Servers return these values, but clients must always check output parameters to ensure that they contain valid values. For more information, see <a href="/windows/desktop/WinAuto/checking-iaccessible-return-values">Checking IAccessible Return Values</a>.

<table>
<tr>
<th>Error</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No parent exists for this object.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accchild">IAccessible::get_accChild</a>



<a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a>



<a href="/windows/desktop/WinAuto/object-navigation-properties-and-methods">Object Navigation Properties and Methods</a>