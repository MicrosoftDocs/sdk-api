---
UID: NF:oleacc.IAccPropServer.GetPropValue
title: IAccPropServer::GetPropValue (oleacc.h)
description: Retrieves a property value for an accessible element.
helpviewer_keywords: ["GetPropValue","GetPropValue method [Windows Accessibility]","GetPropValue method [Windows Accessibility]","IAccPropServer interface","IAccPropServer interface [Windows Accessibility]","GetPropValue method","IAccPropServer.GetPropValue","IAccPropServer::GetPropValue","_msaa_IAccPropServer_GetPropValue","msaa.iaccpropserver_iaccpropserver__getpropvalue","oleacc/IAccPropServer::GetPropValue","winauto.iaccpropserver_iaccpropserver__getpropvalue"]
old-location: winauto\iaccpropserver_iaccpropserver__getpropvalue.htm
tech.root: WinAuto
ms.assetid: 35cb2935-c41b-4588-9199-23789af23b72
ms.date: 12/05/2018
ms.keywords: GetPropValue, GetPropValue method [Windows Accessibility], GetPropValue method [Windows Accessibility],IAccPropServer interface, IAccPropServer interface [Windows Accessibility],GetPropValue method, IAccPropServer.GetPropValue, IAccPropServer::GetPropValue, _msaa_IAccPropServer_GetPropValue, msaa.iaccpropserver_iaccpropserver__getpropvalue, oleacc/IAccPropServer::GetPropValue, winauto.iaccpropserver_iaccpropserver__getpropvalue
req.header: oleacc.h
req.include-header: OleAcc.h Include Initguid.h first.
req.target-type: Windows
req.target-min-winverclnt: Windows Vista or Windows XP
req.target-min-winversvr: Windows Server 2003
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
req.dll: Oleacc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 2.0 RDK on Windows NT 4.0 with SP6 and later and Windows 98
ms.custom: 19H1
f1_keywords:
 - IAccPropServer::GetPropValue
 - oleacc/IAccPropServer::GetPropValue
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
 - IAccPropServer.GetPropValue
---

# IAccPropServer::GetPropValue


## -description

Retrieves a property value for an accessible element.

## -parameters

### -param pIDString [in]

Type: <b>const  BYTE*</b>

Contains a string that identifies the property  being requested.

### -param dwIDStringLen [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Specifies the length of the identity string specified by the <i>pIDString</i> parameter.

### -param idProp [in]

Type: <b>MSAAPROPID</b>

Specifies a GUID indicating the desired property.

### -param pvarValue [out]

Type: <b>VARIANT*</b>

Specifies the value of the overridden property. This parameter is valid only if <i>pfHasProp</i> is <b>TRUE</b>. The server must set this to VT_EMPTY if <i>pfHasProp</i> is set to <b>FALSE</b>.

### -param pfHasProp [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

Indicates whether the server is supplying a value for the requested property. The server should set this to <b>TRUE</b> if it is returning an overriding property or to <b>FALSE</b> if it is not returning a property (in which case it should also set <i>pvarValue</i> to VT_EMPTY).

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Return S_OK, except under exceptional error conditions such as low memory. If the specified property is not overridden, then <i>pfHasProp</i> should be set to <b>FALSE</b> and <i>pvarValue</i> should be set to VT_EMPTY by the server.

## -remarks

If a single callback object is registered for annotating multiple accessible elements, the identity string can be used to determine which element this request refers to.

If the accessible element is <b>HWND</b>-based, <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-decomposehwndidentitystring">IAccPropServices::DecomposeHwndIdentityString</a> can be used to extract the HWND/idObject/idChild from the identity string.

If the callback has a value to return for the specified property, it should return it in <i>pvarValue</i> and set <i>pfHasProp</i> to <b>TRUE</b>. Otherwise it should set <i>pvarValue</i> to VT_EMPTY and set <i>pfHasProp</i> to <b>FALSE</b>. In this latter case, the original <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface pointer will be used to obtain a value for this property.