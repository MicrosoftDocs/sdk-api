---
UID: NF:wsmandisp.IWSManEx.EnumerationFlagReturnObject
title: IWSManEx::EnumerationFlagReturnObject
author: windows-sdk-content
description: Returns the value of the enumeration constant EnumerationFlagReturnObject for use in the flags parameter of the IWSManSession::Enumerate method.
old-location: winrm\iwsmanex_enumerationflagreturnobject.htm
tech.root: winrm
ms.assetid: 19993342-a805-4d92-ac80-40f568b53800
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EnumerationFlagReturnObject, EnumerationFlagReturnObject method [Windows Remote Management], EnumerationFlagReturnObject method [Windows Remote Management],IWSManEx interface, IWSManEx interface [Windows Remote Management],EnumerationFlagReturnObject method, IWSManEx.EnumerationFlagReturnObject, IWSManEx::EnumerationFlagReturnObject, winrm.iwsmanex_enumerationflagreturnobject, wsmandisp/IWSManEx::EnumerationFlagReturnObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
---

# IWSManEx::EnumerationFlagReturnObject


## -description


The <b>IWSManEx::EnumerationFlagReturnObject</b> method returns the value of the enumeration constant <b>EnumerationFlagReturnObject</b> for use in the <i>flags</i> parameter of the <a href="https://msdn.microsoft.com/b1a4815e-93aa-4a30-a67e-c52fd06c1ee1">IWSManSession::Enumerate</a> method.

<b>EnumerationFlagReturnObject</b> is a constant in the <b>_WSManEnumFlags</b> enumeration and is described in <a href="https://msdn.microsoft.com/c0f2763b-a549-43d5-84a6-8cebf33a1ea2">Enumeration Constants</a>.


## -parameters




### -param flags [out]

The value of the constant.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/23fdd9d9-4a78-4c01-8e5d-c8007f39d5d6">IWSManEx</a>



<a href="https://msdn.microsoft.com/3e016080-339f-4bda-bfd2-f912e090981f">IWSManSession</a>
 

 

