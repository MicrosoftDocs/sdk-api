---
UID: NF:wsmandisp.IWSManEx.EnumerationFlagNonXmlText
title: IWSManEx::EnumerationFlagNonXmlText
author: windows-sdk-content
description: Returns the value of the enumeration constant WSManFlagNonXmlText for use in the flags parameter of the IWSManSession::Enumerate method.
old-location: winrm\iwsmanex_enumerationflagnonxmltext.htm
old-project: WinRM
ms.assetid: f94dc9cc-a4c5-44b8-9ace-63b80b1087d2
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: EnumerationFlagNonXmlText, EnumerationFlagNonXmlText method [Windows Remote Management], EnumerationFlagNonXmlText method [Windows Remote Management],IWSManEx interface, IWSManEx interface [Windows Remote Management],EnumerationFlagNonXmlText method, IWSManEx.EnumerationFlagNonXmlText, IWSManEx::EnumerationFlagNonXmlText, winrm.iwsmanex_enumerationflagnonxmltext, wsmandisp/IWSManEx::EnumerationFlagNonXmlText
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WSManProxyAuthenticationFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManEx.EnumerationFlagNonXmlText
product: Windows
targetos: Windows
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSManEx::EnumerationFlagNonXmlText


## -description


The 
    <b>IWSManEx::EnumerationFlagNonXmlText</b> 
    method returns the value of the enumeration constant <b>WSManFlagNonXmlText</b> for 
    use in the <i>flags</i> parameter of the 
    <a href="https://msdn.microsoft.com/b1a4815e-93aa-4a30-a67e-c52fd06c1ee1">IWSManSession::Enumerate</a> method.

<b>WSManFlagNonXmlText</b> is a constant in the 
    <b>__WSManEnumFlags</b> enumeration. For more information, see 
    <a href="https://msdn.microsoft.com/c0f2763b-a549-43d5-84a6-8cebf33a1ea2">Enumeration Constants</a>.


## -parameters




### -param flags [out]

The value of the constant.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/23fdd9d9-4a78-4c01-8e5d-c8007f39d5d6">IWSManEx</a>



<a href="https://msdn.microsoft.com/3e016080-339f-4bda-bfd2-f912e090981f">IWSManSession</a>
 

 

