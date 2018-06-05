---
UID: NN:wmsdkidl.IWMOutputMediaProps
title: IWMOutputMediaProps
author: windows-sdk-content
description: The IWMOutputMediaProps interface is used to retrieve the properties of an output stream.An IWMOutputMediaProps object is created by a call to IWMReader::GetOutputFormat or IWMReader::GetOutputProps.
old-location: wmformat\iwmoutputmediaprops.htm
old-project: wmformat
ms.assetid: 8cf40db5-3902-4c14-b728-98da90567e89
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWMOutputMediaProps, IWMOutputMediaProps interface [windows Media Format], IWMOutputMediaProps interface [windows Media Format],described, IWMOutputMediaPropsInterface, wmformat.iwmoutputmediaprops, wmsdkidl/IWMOutputMediaProps
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
tech.root: 
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmsdkidl.h
api_name:
-	IWMOutputMediaProps
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMOutputMediaProps interface


## -description



The <b>IWMOutputMediaProps</b> interface is used to retrieve the properties of an output stream.

An <b>IWMOutputMediaProps</b> object is created by a call to <a href="https://msdn.microsoft.com/e73d13b9-3fca-4de1-b89d-5cacc6311cd3">IWMReader::GetOutputFormat</a> or <a href="https://msdn.microsoft.com/8958abd0-cc2b-4d02-a831-c998d468fb06">IWMReader::GetOutputProps</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMOutputMediaProps</b> interface inherits from <a href="https://msdn.microsoft.com/a81abd80-e487-421c-ba81-9b43c4233084">IWMMediaProps</a>. <b>IWMOutputMediaProps</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMOutputMediaProps</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93367398-07aa-4c14-85c8-e3a904bd4564">GetConnectionName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the connection to be used for output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65251316-c98f-46a3-a0cf-164531ef0b46">GetStreamGroupName</a>
</td>
<td align="left" width="63%">
Returns an empty string.

</td>
</tr>
</table> 

For information on which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/96fa7c66-59a0-4eb3-ace4-a827b139f978">Output Media Properties Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/d901ac66-d4b3-4256-bd7b-53cccb3de644">IWMInputMediaProps Interface</a>



<a href="https://msdn.microsoft.com/a81abd80-e487-421c-ba81-9b43c4233084">IWMMediaProps</a>



<a href="https://msdn.microsoft.com/0a5325d1-880b-4d65-96af-9d311dca989b">IWMReader::SetOutputProps</a>



<a href="https://msdn.microsoft.com/87d16641-3d28-4bad-962b-8ec808cd7877">IWMReaderTypeNegotiation::TryOutputProps</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

