---
UID: NN:wsmandisp.IWSManResourceLocator
title: IWSManResourceLocator (wsmandisp.h)
description: Supplies the path to a resource. You can use an IWSManResourceLocator object instead of a resource URI in IWSManSession object operations such as IWSManSession.Get, IWSManSession.Put, or IWSManSession.Enumerate.
helpviewer_keywords: ["IWSManResourceLocator","IWSManResourceLocator interface [Windows Remote Management]","IWSManResourceLocator interface [Windows Remote Management]","described","winrm.iwsmanresourcelocator","wsmandisp/IWSManResourceLocator"]
old-location: winrm\iwsmanresourcelocator.htm
tech.root: winrm
ms.assetid: 7b3dcb53-d02c-4ba6-973d-1493ba442387
ms.date: 12/05/2018
ms.keywords: IWSManResourceLocator, IWSManResourceLocator interface [Windows Remote Management], IWSManResourceLocator interface [Windows Remote Management],described, winrm.iwsmanresourcelocator, wsmandisp/IWSManResourceLocator
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
 - IWSManResourceLocator
 - wsmandisp/IWSManResourceLocator
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
 - IWSManResourceLocator
---

# IWSManResourceLocator interface


## -description

 Supplies the path to a resource. You can use an <b>IWSManResourceLocator</b> object instead of a <a href="/windows/desktop/WinRM/windows-remote-management-glossary">resource URI</a> in <a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmansession">IWSManSession</a> object operations such as <a href="/windows/desktop/WinRM/session-get">IWSManSession.Get</a>, <a href="/windows/desktop/WinRM/session-put">IWSManSession.Put</a>, or <a href="/windows/desktop/WinRM/session-enumerate">IWSManSession.Enumerate</a>.

## -inheritance

The <b>IWSManResourceLocator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSManResourceLocator</b> also has these types of members:

## -remarks

The corresponding scripting object is <a href="/windows/desktop/WinRM/resourcelocator">ResourceLocator</a>.

## -see-also

<a href="/windows/desktop/WinRM/resourcelocator">ResourceLocator</a>



<a href="/windows/desktop/WinRM/windows-remote-management-reference">Windows Remote Management Reference</a>
