---
UID: NF:wsmandisp.IWSManEx.EnumerationFlagHierarchyShallow
title: IWSManEx::EnumerationFlagHierarchyShallow (wsmandisp.h)
description: Returns the value of the enumeration constant EnumerationFlagHierarchyShallow for use in the flags parameter of the IWSManSession::Enumerate method.
old-location: winrm\iwsmanex_enumerationflaghierarchyshallow.htm
tech.root: winrm
ms.assetid: 590cf20d-56bc-4472-9d40-cc423bfb00df
ms.date: 12/05/2018
ms.keywords: EnumerationFlagHierarchyShallow, EnumerationFlagHierarchyShallow method [Windows Remote Management], EnumerationFlagHierarchyShallow method [Windows Remote Management],IWSManEx interface, IWSManEx interface [Windows Remote Management],EnumerationFlagHierarchyShallow method, IWSManEx.EnumerationFlagHierarchyShallow, IWSManEx::EnumerationFlagHierarchyShallow, winrm.iwsmanex_enumerationflaghierarchyshallow, wsmandisp/IWSManEx::EnumerationFlagHierarchyShallow
ms.topic: method
f1_keywords:
- wsmandisp/IWSManEx.EnumerationFlagHierarchyShallow
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- WSMAuto.dll
api_name:
- IWSManEx.EnumerationFlagHierarchyShallow
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSManEx::EnumerationFlagHierarchyShallow


## -description


The <b>IWSManEx::EnumerationFlagHierarchyShallow</b> method returns the value of the enumeration constant <b>EnumerationFlagHierarchyShallow</b> for use in the <i>flags</i> parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-enumerate">IWSManSession::Enumerate</a> method.

<b>EnumerationFlagHierarchyShallow</b> is a constant in the <b>_WSManEnumFlags</b> enumeration and is described in <a href="https://docs.microsoft.com/windows/desktop/WinRM/enumeration-constants">Enumeration Constants</a>.


## -parameters




### -param flags [out]

The value of the constant.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanex">IWSManEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmansession">IWSManSession</a>
 

 

