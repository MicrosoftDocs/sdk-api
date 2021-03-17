---
UID: NF:fhcfg.IFhConfigMgr.GetDefaultTarget
title: IFhConfigMgr::GetDefaultTarget (fhcfg.h)
description: Returns a pointer to an IFhTarget interface that can be used to query information about the currently assigned backup target.
helpviewer_keywords: ["FhConfigMgr class [Windows API]","GetDefaultTarget method","GetDefaultTarget","GetDefaultTarget method [Windows API]","GetDefaultTarget method [Windows API]","FhConfigMgr class","GetDefaultTarget method [Windows API]","IFhConfigMgr interface","IFhConfigMgr interface [Windows API]","GetDefaultTarget method","IFhConfigMgr.GetDefaultTarget","IFhConfigMgr::GetDefaultTarget","fhcfg/IFhConfigMgr::GetDefaultTarget","winprog.ifhconfigmgr_getdefaulttarget"]
old-location: winprog\ifhconfigmgr_getdefaulttarget.htm
tech.root: winprog
ms.assetid: 570CB5FD-7586-41AD-84A6-DA6966B18E91
ms.date: 12/05/2018
ms.keywords: FhConfigMgr class [Windows API],GetDefaultTarget method, GetDefaultTarget, GetDefaultTarget method [Windows API], GetDefaultTarget method [Windows API],FhConfigMgr class, GetDefaultTarget method [Windows API],IFhConfigMgr interface, IFhConfigMgr interface [Windows API],GetDefaultTarget method, IFhConfigMgr.GetDefaultTarget, IFhConfigMgr::GetDefaultTarget, fhcfg/IFhConfigMgr::GetDefaultTarget, winprog.ifhconfigmgr_getdefaulttarget
req.header: fhcfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fhcfg.idl
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
 - IFhConfigMgr::GetDefaultTarget
 - fhcfg/IFhConfigMgr::GetDefaultTarget
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fhcfg.h
api_name:
 - IFhConfigMgr.GetDefaultTarget
 - FhConfigMgr.GetDefaultTarget
---

# IFhConfigMgr::GetDefaultTarget


## -description

Returns a pointer to an <a href="/windows/desktop/api/fhcfg/nn-fhcfg-ifhtarget">IFhTarget</a> interface that can be used to query information about the currently assigned backup target.

> [!NOTE] 
> **IFhConfigMgr** is deprecated and may be altered or unavailable in future releases.

## -parameters

### -param DefaultTarget [out]

Receives a pointer to the <a href="/windows/desktop/api/fhcfg/nn-fhcfg-ifhtarget">IFhTarget</a> interface of an object that represents the currently assigned default target, or <b>NULL</b> if there is no default target.

## -returns

<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b>  value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.

## -remarks

If no backup target is currently assigned, this method returns <code>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</code>.

## -see-also

<a href="/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a>



<a href="/windows/desktop/api/fhcfg/nn-fhcfg-ifhconfigmgr">IFhConfigMgr</a>



<a href="/windows/desktop/api/fhcfg/nn-fhcfg-ifhtarget">IFhTarget</a>