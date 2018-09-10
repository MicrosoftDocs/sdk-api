---
UID: NN:wmsdkidl.IWMStatusCallback
title: IWMStatusCallback
author: windows-sdk-content
description: The IWMStatusCallback interface is implemented by the application to receive status information from various objects.
old-location: wmformat\iwmstatuscallback.htm
tech.root: wmformat
ms.assetid: a8d8eed8-0a87-40ce-b1bf-2d476c2e4ae3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWMStatusCallback, IWMStatusCallback interface [windows Media Format], IWMStatusCallback interface [windows Media Format],described, IWMStatusCallbackInterface, wmformat.iwmstatuscallback, wmsdkidl/IWMStatusCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMStatusCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMStatusCallback interface


## -description



The <b>IWMStatusCallback</b> interface is implemented by the application to receive status information from various objects.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMStatusCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMStatusCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMStatusCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">OnStatus</a>
</td>
<td align="left" width="63%">
Called when status information must be communicated to the host application. This happens routinely when an ASF file is being opened and read, and when errors occur during reading.

</td>
</tr>
</table> 


## -remarks



The following methods and functions associate an implementation of this interface with an object:

<ul>
<li>
<a href="https://msdn.microsoft.com/67dfb0df-4883-49e1-a085-0b78db3967d0">IWMIndexer::StartIndexing</a>
</li>
<li>
<a href="https://msdn.microsoft.com/714971d7-8ccb-41fa-92b2-802a503ae228">IWMLicenseBackup::BackupLicenses</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2d645b3a-e856-4745-b80a-89a3bc2b38bd">IWMLicenseRestore::RestoreLicenses</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ab5b7f9e-b647-4121-abb3-2c9deb1f50cc">IWMReader::Open</a>
</li>
<li>
<a href="https://msdn.microsoft.com/69d12e5c-23fd-4d4b-959e-fe7979bf3fdb">IWMRegisterCallback::Advise</a>
</li>
<li>
<a href="https://msdn.microsoft.com/529a5066-df03-4747-bca5-10e3f223d4d2">WMCreateBackupRestorer</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/69b897a8-cc26-445d-9d41-b917b399fb14">IWMReaderCallback</a>



<a href="https://msdn.microsoft.com/9d18961a-5ea4-4f3e-b473-7399e155f800">IWMReaderCallbackAdvanced</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>
 

 

