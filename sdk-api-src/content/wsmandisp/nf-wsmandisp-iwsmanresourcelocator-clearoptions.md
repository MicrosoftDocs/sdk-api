---
UID: NF:wsmandisp.IWSManResourceLocator.ClearOptions
title: IWSManResourceLocator::ClearOptions (wsmandisp.h)
description: Removes any options from the ResourceLocator object.
helpviewer_keywords: ["ClearOptions","ClearOptions method [Windows Remote Management]","ClearOptions method [Windows Remote Management]","IWSManResourceLocator interface","IWSManResourceLocator interface [Windows Remote Management]","ClearOptions method","IWSManResourceLocator.ClearOptions","IWSManResourceLocator::ClearOptions","winrm.iwsmanresourcelocator_clearoptions","wsmandisp/IWSManResourceLocator::ClearOptions"]
old-location: winrm\iwsmanresourcelocator_clearoptions.htm
tech.root: winrm
ms.assetid: 4c71948d-2321-41b5-b961-c4a514830b26
ms.date: 12/05/2018
ms.keywords: ClearOptions, ClearOptions method [Windows Remote Management], ClearOptions method [Windows Remote Management],IWSManResourceLocator interface, IWSManResourceLocator interface [Windows Remote Management],ClearOptions method, IWSManResourceLocator.ClearOptions, IWSManResourceLocator::ClearOptions, winrm.iwsmanresourcelocator_clearoptions, wsmandisp/IWSManResourceLocator::ClearOptions
f1_keywords:
- wsmandisp/IWSManResourceLocator.ClearOptions
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
- IWSManResourceLocator.ClearOptions
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSManResourceLocator::ClearOptions


## -description


Removes any <a href="https://docs.microsoft.com/windows/desktop/WinRM/windows-remote-management-glossary">options</a> from the <a href="https://docs.microsoft.com/windows/desktop/WinRM/resourcelocator">ResourceLocator</a> object. You can provide a <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanresourcelocator">ResourceLocator</a> object instead of specifying a resource URI in <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmansession">IWSManSession</a> object operations such as <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-get">Get</a>, <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-put">Put</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-enumerate">Enumerate</a>.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanresourcelocator">IWSManResourceLocator</a>



<a href="https://docs.microsoft.com/windows/desktop/WinRM/resourcelocator-clearoptions">ResourceLocator.ClearOptions</a>
 

 

