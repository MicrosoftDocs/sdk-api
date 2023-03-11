---
UID: NF:wsmandisp.IWSManResourceLocator.get_ResourceURI
title: IWSManResourceLocator::get_ResourceURI (wsmandisp.h)
description: The resource URI of the requested resource. This property can contain only the path, not a query string for specific instances. (Get)
helpviewer_keywords: ["IWSManResourceLocator interface [Windows Remote Management]","ResourceURI property","IWSManResourceLocator.ResourceURI","IWSManResourceLocator.get_ResourceURI","IWSManResourceLocator::ResourceURI","IWSManResourceLocator::get_ResourceURI","IWSManResourceLocator::put_ResourceURI","ResourceURI property [Windows Remote Management]","ResourceURI property [Windows Remote Management]","IWSManResourceLocator interface","ResourceURI property [Windows Remote Management]","WSMan object","WSMan object [Windows Remote Management]","ResourceURI property","get_ResourceURI","winrm.iwsmanresourcelocator_resourceuri","wsmandisp/IWSManResourceLocator::ResourceURI","wsmandisp/IWSManResourceLocator::get_ResourceURI","wsmandisp/IWSManResourceLocator::put_ResourceURI"]
old-location: winrm\iwsmanresourcelocator_resourceuri.htm
tech.root: winrm
ms.assetid: 8ae490a3-ae6d-46e4-9a51-5a1e9c80cf77
ms.date: 12/05/2018
ms.keywords: IWSManResourceLocator interface [Windows Remote Management],ResourceURI property, IWSManResourceLocator.ResourceURI, IWSManResourceLocator.get_ResourceURI, IWSManResourceLocator::ResourceURI, IWSManResourceLocator::get_ResourceURI, IWSManResourceLocator::put_ResourceURI, ResourceURI property [Windows Remote Management], ResourceURI property [Windows Remote Management],IWSManResourceLocator interface, ResourceURI property [Windows Remote Management],WSMan object, WSMan object [Windows Remote Management],ResourceURI property, get_ResourceURI, winrm.iwsmanresourcelocator_resourceuri, wsmandisp/IWSManResourceLocator::ResourceURI, wsmandisp/IWSManResourceLocator::get_ResourceURI, wsmandisp/IWSManResourceLocator::put_ResourceURI
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
 - IWSManResourceLocator::get_ResourceURI
 - wsmandisp/IWSManResourceLocator::get_ResourceURI
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
 - IWSManResourceLocator.ResourceURI
 - IWSManResourceLocator.get_ResourceURI
 - IWSManResourceLocator.put_ResourceURI
 - WSMan.ResourceURI
---

# IWSManResourceLocator::get_ResourceURI


## -description

The <a href="/windows/desktop/WinRM/windows-remote-management-glossary">resource URI</a> of the requested resource. This property can contain only the path, not a query string for specific instances.

This property is read/write.

## -parameters

## -remarks

<a href="/windows/desktop/WinRM/resourcelocator">ResourceLocator</a> is the corresponding scripting object for the <a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanresourcelocator">IWSManResourceLocator</a> interface.

The following is an example of a proper path for  <b>ResourceURI</b>.


``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
```

The following path does not work because it  contains a key for a specific instance. Use the <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanresourcelocator-addselector">IWSManResourceLocator::AddSelector</a> method to specify a particular instance.


``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
```

The corresponding scripting method is <a href="/windows/desktop/WinRM/resourcelocator-resourceuri">ResourceLocator.ResourceURI</a>.

## -see-also

<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanresourcelocator">IWSManResourceLocator</a>



<a href="/windows/desktop/WinRM/resourcelocator-resourceuri">ResourceLocator.ResourceURI</a>
