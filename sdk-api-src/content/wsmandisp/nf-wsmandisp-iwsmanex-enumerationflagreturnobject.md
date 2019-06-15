---
UID: NF:wsmandisp.IWSManEx.EnumerationFlagReturnObject
title: IWSManEx::EnumerationFlagReturnObject (wsmandisp.h)
author: windows-sdk-content
description: Returns the value of the enumeration constant EnumerationFlagReturnObject for use in the flags parameter of the IWSManSession::Enumerate method.
old-location: winrm\iwsmanex_enumerationflagreturnobject.htm
tech.root: winrm
ms.assetid: 19993342-a805-4d92-ac80-40f568b53800
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumerationFlagReturnObject, EnumerationFlagReturnObject method [Windows Remote Management], EnumerationFlagReturnObject method [Windows Remote Management],IWSManEx interface, IWSManEx interface [Windows Remote Management],EnumerationFlagReturnObject method, IWSManEx.EnumerationFlagReturnObject, IWSManEx::EnumerationFlagReturnObject, winrm.iwsmanex_enumerationflagreturnobject, wsmandisp/IWSManEx::EnumerationFlagReturnObject
ms.topic: method
f1_keywords: ["wsmandisp/IWSManEx.EnumerationFlagReturnObject"]
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
 - IWSManEx.EnumerationFlagReturnObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSManEx::EnumerationFlagReturnObject


## -description


The <b>IWSManEx::EnumerationFlagReturnObject</b> method returns the value of the enumeration constant <b>EnumerationFlagReturnObject</b> for use in the <i>flags</i> parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-enumerate">IWSManSession::Enumerate</a> method.

<b>EnumerationFlagReturnObject</b> is a constant in the <b>_WSManEnumFlags</b> enumeration and is described in <a href="https://docs.microsoft.com/windows/desktop/WinRM/enumeration-constants">Enumeration Constants</a>.


## -parameters




### -param flags [out]

The value of the constant.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanex">IWSManEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmansession">IWSManSession</a>
 

 

