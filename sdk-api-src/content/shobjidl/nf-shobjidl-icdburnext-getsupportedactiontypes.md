---
UID: NF:shobjidl.ICDBurnExt.GetSupportedActionTypes
title: ICDBurnExt::GetSupportedActionTypes (shobjidl.h)
description: Determines the supported data type for a CD writing extension.
helpviewer_keywords: ["CDBE_TYPE_ALL","CDBE_TYPE_DATA","CDBE_TYPE_MUSIC","GetSupportedActionTypes","GetSupportedActionTypes method [Windows Shell]","GetSupportedActionTypes method [Windows Shell]","ICDBurnExt interface","ICDBurnExt interface [Windows Shell]","GetSupportedActionTypes method","ICDBurnExt.GetSupportedActionTypes","ICDBurnExt::GetSupportedActionTypes","_shell_ICDBurnExt_GetSupportedActionTypes","shell.ICDBurnExt_GetSupportedActionTypes","shobjidl/ICDBurnExt::GetSupportedActionTypes"]
old-location: shell\ICDBurnExt_GetSupportedActionTypes.htm
tech.root: shell
ms.assetid: 46d0fe58-b8aa-42a8-811e-9762185bb8cc
ms.date: 12/05/2018
ms.keywords: CDBE_TYPE_ALL, CDBE_TYPE_DATA, CDBE_TYPE_MUSIC, GetSupportedActionTypes, GetSupportedActionTypes method [Windows Shell], GetSupportedActionTypes method [Windows Shell],ICDBurnExt interface, ICDBurnExt interface [Windows Shell],GetSupportedActionTypes method, ICDBurnExt.GetSupportedActionTypes, ICDBurnExt::GetSupportedActionTypes, _shell_ICDBurnExt_GetSupportedActionTypes, shell.ICDBurnExt_GetSupportedActionTypes, shobjidl/ICDBurnExt::GetSupportedActionTypes
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - ICDBurnExt::GetSupportedActionTypes
 - shobjidl/ICDBurnExt::GetSupportedActionTypes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - ICDBurnExt.GetSupportedActionTypes
---

# ICDBurnExt::GetSupportedActionTypes


## -description

Determines the supported data type for a CD writing extension.

## -parameters

### -param pdwActions [out]

Type: <b>CDBE_ACTIONS*</b>

One of the following values indicating the supported type.



#### CDBE_TYPE_MUSIC (0x00000001)

0x00000001. Music files are supported. The CD writing extension is invoked for the <b>Copy to audio CD</b> task in the My Music folder.



#### CDBE_TYPE_DATA (0x00000002)

0x00000002. Data files are supported. The CD writing extension is excluded from <b>Copy to audio CD</b>.



#### CDBE_TYPE_ALL ((int)0xFFFFFFFF)

(int)0xFFFFFFFF. All files are supported. The CD writing extension is invoked for the <b>Copy to audio CD</b> task in the My Music folder.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

