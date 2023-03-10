---
UID: NF:wsmandisp.IWSManResourceLocator.get_FragmentDialect
title: IWSManResourceLocator::get_FragmentDialect (wsmandisp.h)
description: Gets or sets the language dialect for a resource fragment dialect when IWSManResourceLocator is used in IWSManSession object methods such as Get, Put, or Enumerate. (Get)
helpviewer_keywords: ["FragmentDialect property [Windows Remote Management]","FragmentDialect property [Windows Remote Management]","IWSManResourceLocator interface","IWSManResourceLocator interface [Windows Remote Management]","FragmentDialect property","IWSManResourceLocator.FragmentDialect","IWSManResourceLocator.get_FragmentDialect","IWSManResourceLocator::FragmentDialect","IWSManResourceLocator::get_FragmentDialect","IWSManResourceLocator::put_FragmentDialect","get_FragmentDialect","winrm.iwsmanresourcelocator_fragmentdialect","wsmandisp/IWSManResourceLocator::FragmentDialect","wsmandisp/IWSManResourceLocator::get_FragmentDialect","wsmandisp/IWSManResourceLocator::put_FragmentDialect"]
old-location: winrm\iwsmanresourcelocator_fragmentdialect.htm
tech.root: winrm
ms.assetid: eb458fc4-ddcc-42a2-8dd3-05498e035de2
ms.date: 12/05/2018
ms.keywords: FragmentDialect property [Windows Remote Management], FragmentDialect property [Windows Remote Management],IWSManResourceLocator interface, IWSManResourceLocator interface [Windows Remote Management],FragmentDialect property, IWSManResourceLocator.FragmentDialect, IWSManResourceLocator.get_FragmentDialect, IWSManResourceLocator::FragmentDialect, IWSManResourceLocator::get_FragmentDialect, IWSManResourceLocator::put_FragmentDialect, get_FragmentDialect, winrm.iwsmanresourcelocator_fragmentdialect, wsmandisp/IWSManResourceLocator::FragmentDialect, wsmandisp/IWSManResourceLocator::get_FragmentDialect, wsmandisp/IWSManResourceLocator::put_FragmentDialect
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
 - IWSManResourceLocator::get_FragmentDialect
 - wsmandisp/IWSManResourceLocator::get_FragmentDialect
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
 - IWSManResourceLocator.FragmentDialect
 - IWSManResourceLocator.get_FragmentDialect
 - IWSManResourceLocator.put_FragmentDialect
---

# IWSManResourceLocator::get_FragmentDialect


## -description

Gets or sets the language dialect for a <a href="/windows/desktop/WinRM/windows-remote-management-glossary">resource</a> <a href="/windows/desktop/WinRM/windows-remote-management-glossary">fragment</a> <i>dialect</i> when <a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanresourcelocator">IWSManResourceLocator</a> is used in <a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmansession">IWSManSession</a> object methods such as <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-get">Get</a>, <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-put">Put</a>, or <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-enumerate">Enumerate</a>. A fragment represents one property or part of a resource. You can provide an <a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanresourcelocator">IWSManResourceLocator</a> object instead of specifying a <a href="/windows/desktop/WinRM/windows-remote-management-glossary">resource URI</a> in <a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmansession">IWSManSession</a> object operations. 

This property is read/write.

## -parameters

## -remarks

The dialect string defaults to the XPath 1.0 specification. For more information, see <a href="https://www.w3.org/TR/xpath">http://www.w3.org/TR/xpath</a>.

## -see-also

<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanresourcelocator">IWSManResourceLocator</a>



<a href="/windows/desktop/WinRM/resourcelocator-fragmentdialect">ResourceLocator.FragmentDialect</a>
