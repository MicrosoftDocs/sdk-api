---
UID: NF:wsmandisp.IWSManResourceLocator.AddSelector
title: IWSManResourceLocator::AddSelector (wsmandisp.h)
description: Adds a selector to the ResourceLocator object. The selector specifies a particular instance of a resource.
old-location: winrm\iwsmanresourcelocator_addselector.htm
tech.root: winrm
ms.assetid: 2f6c1169-8e2a-4919-9a1a-856dbe41a9ce
ms.date: 12/05/2018
ms.keywords: AddSelector, AddSelector method [Windows Remote Management], AddSelector method [Windows Remote Management],IWSManResourceLocator interface, IWSManResourceLocator interface [Windows Remote Management],AddSelector method, IWSManResourceLocator.AddSelector, IWSManResourceLocator::AddSelector, winrm.iwsmanresourcelocator_addselector, wsmandisp/IWSManResourceLocator::AddSelector
f1_keywords:
- wsmandisp/IWSManResourceLocator.AddSelector
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
- IWSManResourceLocator.AddSelector
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSManResourceLocator::AddSelector


## -description


Adds a <a href="https://docs.microsoft.com/windows/desktop/WinRM/windows-remote-management-glossary">selector</a> to the <a href="https://docs.microsoft.com/windows/desktop/WinRM/resourcelocator">ResourceLocator</a> object. The selector specifies a particular instance of a <i>resource</i>. You can provide an <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanresourcelocator">IWSManResourceLocator</a> object instead of specifying a resource URI in <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmansession">IWSManSession</a> object operations such as <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-get">Get</a>, <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-put">Put</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-enumerate">Enumerate</a>.


## -parameters




### -param resourceSelName [in]

The selector name. For example, when requesting WMI data, this parameter is the key property for a WMI class.


### -param selValue [in]

The selector value. For example, for WMI data, this parameter contains a value for a key property that identifies a specific instance.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanresourcelocator">IWSManResourceLocator</a>



<a href="https://docs.microsoft.com/windows/desktop/WinRM/resourcelocator-addselector">ResourceLocator.AddSelector</a>
 

 

