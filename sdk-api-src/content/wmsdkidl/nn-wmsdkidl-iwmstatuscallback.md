---
UID: NN:wmsdkidl.IWMStatusCallback
title: IWMStatusCallback
author: windows-sdk-content
description: The IWMStatusCallback interface is implemented by the application to receive status information from various objects.
old-location: wmformat\iwmstatuscallback.htm
tech.root: wmformat
ms.assetid: a8d8eed8-0a87-40ce-b1bf-2d476c2e4ae3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMStatusCallback, IWMStatusCallback interface [windows Media Format], IWMStatusCallback interface [windows Media Format],described, IWMStatusCallbackInterface, wmformat.iwmstatuscallback, wmsdkidl/IWMStatusCallback
ms.prod: windows-hardware
ms.technology: windows-devices
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
<a href="https://msdn.microsoft.com/en-us/library/Dd798545(v=VS.85).aspx">OnStatus</a>
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
<a href="https://msdn.microsoft.com/en-us/library/Dd757208(v=VS.85).aspx">IWMIndexer::StartIndexing</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd757219(v=VS.85).aspx">IWMLicenseBackup::BackupLicenses</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd757224(v=VS.85).aspx">IWMLicenseRestore::RestoreLicenses</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd743597(v=VS.85).aspx">IWMReader::Open</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd743615(v=VS.85).aspx">IWMRegisterCallback::Advise</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd757744(v=VS.85).aspx">WMCreateBackupRestorer</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743493(v=VS.85).aspx">IWMReaderCallback</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743494(v=VS.85).aspx">IWMReaderCallbackAdvanced</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>
 

 

