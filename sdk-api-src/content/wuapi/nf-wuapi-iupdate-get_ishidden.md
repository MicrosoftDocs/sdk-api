---
UID: NF:wuapi.IUpdate.get_IsHidden
title: IUpdate::get_IsHidden (wuapi.h)
description: Gets a Boolean value that indicates whether an update is hidden by a user. (Get)
helpviewer_keywords: ["IUpdate interface [Windows Update Agent]","IsHidden property","IUpdate.IsHidden","IUpdate.get_IsHidden","IUpdate::IsHidden","IUpdate::get_IsHidden","IUpdate::put_IsHidden","IsHidden property [Windows Update Agent]","IsHidden property [Windows Update Agent]","IUpdate interface","get_IsHidden","wua.iupdate_ishidden","wuapi/IUpdate::IsHidden","wuapi/IUpdate::get_IsHidden","wuapi/IUpdate::put_IsHidden"]
old-location: wua\iupdate_ishidden.htm
tech.root: wua
ms.assetid: 229fbb68-cc99-440e-89e1-b9c4e69dd0b3
ms.date: 12/05/2018
ms.keywords: IUpdate interface [Windows Update Agent],IsHidden property, IUpdate.IsHidden, IUpdate.get_IsHidden, IUpdate::IsHidden, IUpdate::get_IsHidden, IUpdate::put_IsHidden, IsHidden property [Windows Update Agent], IsHidden property [Windows Update Agent],IUpdate interface, get_IsHidden, wua.iupdate_ishidden, wuapi/IUpdate::IsHidden, wuapi/IUpdate::get_IsHidden, wuapi/IUpdate::put_IsHidden
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUpdate::get_IsHidden
 - wuapi/IUpdate::get_IsHidden
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdate.IsHidden
 - IUpdate.get_IsHidden
 - IUpdate.put_IsHidden
---

# IUpdate::get_IsHidden


## -description

Gets a Boolean value that indicates whether an update is hidden by a user. Administrators, users, and power users can retrieve the value of this property. However, only administrators and members of the Power Users administrative group can set the value of this property.

This property is read/write.

## -parameters

### -param retval [out, retval]

Type: <b>VARIANT_BOOL*</b>

A pointer to a variable of type <a href="/windows/win32/api/oaidl/ns-oaidl-variant#__variant_name_2__variant_name_3bool">VARIANT_BOOL</a> that receives <b>VARIANT_TRUE</b> if the update is hidden, and <b>VARIANT_FALSE</b> if not.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An attempt to mark a mandatory update as hidden causes an error.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>
