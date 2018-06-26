---
UID: NN:iads.IADsObjectOptions
title: IADsObjectOptions
author: windows-sdk-content
description: Provides a direct mechanism to specify and obtain provider-specific options for manipulating an ADSI object.
old-location: adsi\iadsobjectoptions.htm
old-project: ADSI
ms.assetid: 1884efe5-86f5-4579-a25e-2ff9c9a6ec2a
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IADsObjectOptions, IADsObjectOptions interface [ADSI], IADsObjectOptions interface [ADSI],described, _ds_iadsobjectoptions, adsi.iadsobjectoptions, iads/IADsObjectOptions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsObjectOptions
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsObjectOptions interface


## -description


The <b>IADsObjectOptions</b> interface provides a direct mechanism to specify and obtain provider-specific options for manipulating an ADSI object. Typically, the options apply to search operations of the underlying directory store. The supported options are provider-specific.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsObjectOptions</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IADsObjectOptions</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IADsObjectOptions</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451273">GetOption</a>
</td>
<td align="left" width="63%">
Gets a provider-specific option for a directory object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6e43c99-fc8b-4f34-82cf-8cf30c506859">SetOption</a>
</td>
<td align="left" width="63%">
Sets a provider-specific option for manipulating a directory object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/afb32e03-7e4e-4df9-87c7-db962d62e5f0">ADS_OPTION_ENUM</a>



<a href="https://msdn.microsoft.com/9cd1bb86-313d-4499-97ae-0b53a13a804b">ADS_SECURITY_INFO_ENUM</a>



<a href="https://msdn.microsoft.com/cf41b0c4-7459-49cf-945b-8462c7d19947">Fast Binding Option for Batch Write/Modify Operations</a>



<a href="https://msdn.microsoft.com/b4ac114f-1a23-4be6-af02-0c0d34a8f78f">IADsObjectOptions Interface</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

