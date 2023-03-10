---
UID: NF:shobjidl_core.IAppVisibility.Advise
title: IAppVisibility::Advise (shobjidl_core.h)
description: Registers an advise sink object to receive notification of changes to the display.
helpviewer_keywords: ["Advise","Advise method [Windows Shell]","Advise method [Windows Shell]","IAppVisibility interface","IAppVisibility interface [Windows Shell]","Advise method","IAppVisibility.Advise","IAppVisibility::Advise","shell.IAppVisibility_Advise","shobjidl_core/IAppVisibility::Advise"]
old-location: shell\IAppVisibility_Advise.htm
tech.root: shell
ms.assetid: 602F46EF-014C-4219-9C1F-C1B4371EA456
ms.date: 12/05/2018
ms.keywords: Advise, Advise method [Windows Shell], Advise method [Windows Shell],IAppVisibility interface, IAppVisibility interface [Windows Shell],Advise method, IAppVisibility.Advise, IAppVisibility::Advise, shell.IAppVisibility_Advise, shobjidl_core/IAppVisibility::Advise
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
ms.custom: 19H1
f1_keywords:
 - IAppVisibility::Advise
 - shobjidl_core/IAppVisibility::Advise
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IAppVisibility.Advise
---

# IAppVisibility::Advise


## -description

Registers an advise sink object to receive notification of changes to the display.

## -parameters

### -param pCallback [in]

The client's advise sink that receives outgoing calls from the connection point.

### -param pdwCookie [out]

A token that uniquely identifies this connection. Use this token to delete the connection by passing it to the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iappvisibility-unadvise">Unadvise</a> method.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pdwCookie</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iappvisibility">IAppVisibility</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iappvisibilityevents">IAppVisibilityEvents</a>