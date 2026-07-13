---
UID: NF:wsmandisp.IWSManEx.EnumerationFlagHierarchyDeepBasePropsOnly
title: IWSManEx::EnumerationFlagHierarchyDeepBasePropsOnly (wsmandisp.h)
description: Returns the value of the enumeration constant EnumerationFlagHierarchyDeepBasePropsOnly for use in the flags parameter of the IWSManSession::Enumerate method.
helpviewer_keywords: ["EnumerationFlagHierarchyDeepBasePropsOnly","EnumerationFlagHierarchyDeepBasePropsOnly method [Windows Remote Management]","EnumerationFlagHierarchyDeepBasePropsOnly method [Windows Remote Management]","IWSManEx interface","IWSManEx interface [Windows Remote Management]","EnumerationFlagHierarchyDeepBasePropsOnly method","IWSManEx.EnumerationFlagHierarchyDeepBasePropsOnly","IWSManEx::EnumerationFlagHierarchyDeepBasePropsOnly","winrm.iwsmanex_enumerationflaghierarchydeepbasepropsonly","wsmandisp/IWSManEx::EnumerationFlagHierarchyDeepBasePropsOnly"]
old-location: winrm\iwsmanex_enumerationflaghierarchydeepbasepropsonly.htm
tech.root: winrm
ms.assetid: 72528ef3-3e38-4f1f-a686-45c3caa1d9d3
ms.date: 12/05/2018
ms.keywords: EnumerationFlagHierarchyDeepBasePropsOnly, EnumerationFlagHierarchyDeepBasePropsOnly method [Windows Remote Management], EnumerationFlagHierarchyDeepBasePropsOnly method [Windows Remote Management],IWSManEx interface, IWSManEx interface [Windows Remote Management],EnumerationFlagHierarchyDeepBasePropsOnly method, IWSManEx.EnumerationFlagHierarchyDeepBasePropsOnly, IWSManEx::EnumerationFlagHierarchyDeepBasePropsOnly, winrm.iwsmanex_enumerationflaghierarchydeepbasepropsonly, wsmandisp/IWSManEx::EnumerationFlagHierarchyDeepBasePropsOnly
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSManEx::EnumerationFlagHierarchyDeepBasePropsOnly
 - wsmandisp/IWSManEx::EnumerationFlagHierarchyDeepBasePropsOnly
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManEx.EnumerationFlagHierarchyDeepBasePropsOnly
---

# IWSManEx::EnumerationFlagHierarchyDeepBasePropsOnly


## -description

The <b>IWSManEx::EnumerationFlagHierarchyDeepBasePropsOnly</b> method returns the value of the enumeration constant <b>EnumerationFlagHierarchyDeepBasePropsOnly</b> for use in the <i>flags</i> parameter of the <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-enumerate">IWSManSession::Enumerate</a> method.

<b>EnumerationFlagHierarchyDeepBasePropsOnly</b> is a constant in the <b>_WSManEnumFlags</b> enumeration and is described in <a href="/windows/desktop/WinRM/enumeration-constants">Enumeration Constants</a>.

## -parameters

### -param flags [out]

The value of the constant.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanex">IWSManEx</a>



<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmansession">IWSManSession</a>