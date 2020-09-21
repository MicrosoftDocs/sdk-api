---
UID: NF:oleacc.IAccPropServices.SetPropServer
title: IAccPropServices::SetPropServer (oleacc.h)
description: Servers use SetPropServer to specify a callback object to be used to annotate an array of properties for the accessible element.
helpviewer_keywords: ["IAccPropServices interface [Windows Accessibility]","SetPropServer method","IAccPropServices.SetPropServer","IAccPropServices::SetPropServer","SetPropServer","SetPropServer method [Windows Accessibility]","SetPropServer method [Windows Accessibility]","IAccPropServices interface","_msaa_IAccPropServices_SetPropServer","msaa.iaccpropservices_iaccpropservices__setpropserver","oleacc/IAccPropServices::SetPropServer","winauto.iaccpropservices_iaccpropservices__setpropserver"]
old-location: winauto\iaccpropservices_iaccpropservices__setpropserver.htm
tech.root: WinAuto
ms.assetid: 15e43a38-4cb3-43ca-a0fc-28faf49057dc
ms.date: 12/05/2018
ms.keywords: IAccPropServices interface [Windows Accessibility],SetPropServer method, IAccPropServices.SetPropServer, IAccPropServices::SetPropServer, SetPropServer, SetPropServer method [Windows Accessibility], SetPropServer method [Windows Accessibility],IAccPropServices interface, _msaa_IAccPropServices_SetPropServer, msaa.iaccpropservices_iaccpropservices__setpropserver, oleacc/IAccPropServices::SetPropServer, winauto.iaccpropservices_iaccpropservices__setpropserver
req.header: oleacc.h
req.include-header: OleAcc.h Include Initguid.h first.
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: Oleacc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 2.0 RDK on Windows NT 4.0 with SP6 and later and Windows 98
ms.custom: 19H1
f1_keywords:
 - IAccPropServices::SetPropServer
 - oleacc/IAccPropServices::SetPropServer
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
 - IAccPropServices.SetPropServer
---

# IAccPropServices::SetPropServer


## -description

Servers use <b>SetPropServer</b> to specify a callback object to be used to annotate an array of properties for the accessible element. You can also specify whether the annotation is to be applied to this accessible element or to the element and its children. This method is used for <a href="/windows/desktop/WinAuto/server-annotation">server annotation</a>.

If server developers know the <b>HWND</b> of the accessible element they want to annotate, they can use <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-sethwndpropserver">IAccPropServices::SetHwndPropServer</a>.

## -parameters

### -param pIDString [in]

Type: <b>const <a href="/windows/desktop/WinProg/windows-data-types">BYTE</a>*</b>

Identifies the accessible element that is to be annotated.

### -param dwIDStringLen [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Specifies the length of the string identified by the <i>pIDString</i> parameter.

### -param paProps [in]

Type: <b>const MSAAPROPID*</b>

Specifies an array of properties to be handled by the specified callback object.

### -param cProps [in]

Type: <b>int</b>

Specifies an array of properties to be handled by the specified callback object.

### -param pServer [in]

Type: <b>IAccPropServer*</b>

Specifies the callback object that will be invoked when a client requests one of the overridden properties.

### -param annoScope [in]

Type: <b>AnnoScope</b>

May be ANNO_THIS, indicating that the annotation affects the indicated accessible element only; or ANNO_CONTAINER, indicating that it applies to the element and its immediate element children.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK.

Returns E_INVALIDARG if any of the properties in the <i>paProps</i> array are not supported properties, if the identity string is not valid, or if <i>annoScope</i> is not one of ANNO_THIS or ANNO_CONTAINER.

May return other error codes under exceptional error conditions such as low memory.

## -remarks

See the support section for a list of supported properties and their expected types.

The annotation run time will use <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> to increment the reference counter for the <i>pServer</i> callback object appropriately. The caller is free to <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> it after calling this method. The annotation run time will automatically release the callback object after the accessible element being annotated is no longer being used.