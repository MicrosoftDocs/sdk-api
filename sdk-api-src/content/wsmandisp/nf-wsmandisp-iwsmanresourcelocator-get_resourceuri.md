---
UID: NF:wsmandisp.IWSManResourceLocator.get_ResourceURI
title: IWSManResourceLocator::get_ResourceURI (wsmandisp.h)
author: windows-sdk-content
description: The resource URI of the requested resource. This property can contain only the path, not a query string for specific instances.
old-location: winrm\iwsmanresourcelocator_resourceuri.htm
tech.root: winrm
ms.assetid: 8ae490a3-ae6d-46e4-9a51-5a1e9c80cf77
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWSManResourceLocator interface [Windows Remote Management],ResourceURI property, IWSManResourceLocator.ResourceURI, IWSManResourceLocator.get_ResourceURI, IWSManResourceLocator::ResourceURI, IWSManResourceLocator::get_ResourceURI, IWSManResourceLocator::put_ResourceURI, ResourceURI property [Windows Remote Management], ResourceURI property [Windows Remote Management],IWSManResourceLocator interface, ResourceURI property [Windows Remote Management],WSMan object, WSMan object [Windows Remote Management],ResourceURI property, get_ResourceURI, winrm.iwsmanresourcelocator_resourceuri, wsmandisp/IWSManResourceLocator::ResourceURI, wsmandisp/IWSManResourceLocator::get_ResourceURI, wsmandisp/IWSManResourceLocator::put_ResourceURI
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
 - IWSManResourceLocator.ResourceURI
 - IWSManResourceLocator.get_ResourceURI
 - IWSManResourceLocator.put_ResourceURI
 - WSMan.ResourceURI
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSManResourceLocator::get_ResourceURI


## -description


The <a href="https://msdn.microsoft.com/en-us/library/Aa384465(v=VS.85).aspx">resource URI</a> of the requested resource. This property can contain only the path, not a query string for specific instances.

This property is read/write.


## -parameters


## -remarks




<a href="https://msdn.microsoft.com/0904b7eb-d4ce-46a7-bf58-452e7c0d41e9">ResourceLocator</a> is the corresponding scripting object for the <a href="https://msdn.microsoft.com/7b3dcb53-d02c-4ba6-973d-1493ba442387">IWSManResourceLocator</a> interface.

The following is an example of a proper path for  <b>ResourceURI</b>.

<pre class="syntax" xml:space="preserve"><code>"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"</code></pre>
The following path does not work because it  contains a key for a specific instance. Use the <a href="https://msdn.microsoft.com/2f6c1169-8e2a-4919-9a1a-856dbe41a9ce">IWSManResourceLocator::AddSelector</a> method to specify a particular instance.

<pre class="syntax" xml:space="preserve"><code>"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"</code></pre>
The corresponding scripting method is <a href="https://msdn.microsoft.com/adb1e08a-290f-4a23-a6e4-d7567a6b7eee">ResourceLocator.ResourceURI</a>.




## -see-also




<a href="https://msdn.microsoft.com/7b3dcb53-d02c-4ba6-973d-1493ba442387">IWSManResourceLocator</a>



<a href="https://msdn.microsoft.com/adb1e08a-290f-4a23-a6e4-d7567a6b7eee">ResourceLocator.ResourceURI</a>
 

 

