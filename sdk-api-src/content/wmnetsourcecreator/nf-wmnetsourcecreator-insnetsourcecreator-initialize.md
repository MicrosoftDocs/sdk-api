---
UID: NF:wmnetsourcecreator.INSNetSourceCreator.Initialize
title: INSNetSourceCreator::Initialize
author: windows-sdk-content
description: The Initialize method prepares the network source creator for operations. You must call this method before calling any of the other methods in the INSNetSourceCreator interface.
old-location: wmformat\insnetsourcecreator_initialize.htm
tech.root: wmformat
ms.assetid: 53c1a15e-3ced-44e5-b512-b381ae11aa65
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: INSNetSourceCreator interface [windows Media Format],Initialize method, INSNetSourceCreator.Initialize, INSNetSourceCreator::Initialize, INSNetSourceCreatorInitialize, Initialize, Initialize method [windows Media Format], Initialize method [windows Media Format],INSNetSourceCreator interface, wmformat.insnetsourcecreator_initialize, wmnetsourcecreator/INSNetSourceCreator::Initialize
ms.topic: method
req.header: wmnetsourcecreator.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - INSNetSourceCreator.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INSNetSourceCreator::Initialize


## -description



The <b>Initialize</b> method prepares the network source creator for operations. You must call this method before calling any of the other methods in the <b>INSNetSourceCreator</b> interface.




## -parameters






## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method could not allocate memory for an internal resource.

</td>
</tr>
</table>
 




## -remarks



When you are finished using the network source creator, you must call the <a href="https://msdn.microsoft.com/en-us/library/Dd743242(v=VS.85).aspx">Shutdown</a> method to ensure that all resources are released properly.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743239(v=VS.85).aspx">INSNetSourceCreator Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743242(v=VS.85).aspx">INSNetSourceCreator::Shutdown</a>
 

 

