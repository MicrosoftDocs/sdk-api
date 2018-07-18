---
UID: NN:msctf.IEnumTfInputProcessorProfiles
title: IEnumTfInputProcessorProfiles
author: windows-sdk-content
description: The IEnumTfInputProcessorProfiles interface is implemented by TSF manager and used by applications or textservices. This interface can be retrieved by ITfInputProcessorProfileMgr::EnumProfiles and enumerates the registered profiles.
old-location: tsf\ienumtfinputprocessorprofiles.htm
old-project: TSF
ms.assetid: 1a6dd7f9-d348-4c86-8d74-544aaa45581d
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: IEnumTfInputProcessorProfiles, IEnumTfInputProcessorProfiles interface [Text Services Framework], IEnumTfInputProcessorProfiles interface [Text Services Framework],described, _tsf_ienumtfinputprocessorprofiles_ref, msctf/IEnumTfInputProcessorProfiles, tsf.ienumtfinputprocessorprofiles
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.h
api_name:
 - IEnumTfInputProcessorProfiles
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# IEnumTfInputProcessorProfiles interface


## -description


The <b>IEnumTfInputProcessorProfiles</b> interface is implemented by TSF manager and used by applications or textservices. This interface can be retrieved by <a href="https://msdn.microsoft.com/d4728d12-9073-41b8-94bc-eaf7c1df19b6">ITfInputProcessorProfileMgr::EnumProfiles</a> and enumerates the registered profiles.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumTfInputProcessorProfiles</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumTfInputProcessorProfiles</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumTfInputProcessorProfiles</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">
Obtains, from the current position, the specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator object by moving the current position to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926952">Skip</a>
</td>
<td align="left" width="63%">
Moves the current position forward in the enumeration sequence by the specified number of elements.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/9fa722a4-1e3f-4845-aea7-3b24b517f2a5">ITfInputProcessorProfiles
      </a>
 

 

