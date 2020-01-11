---
UID: NN:iads.IADsObjectOptions
title: IADsObjectOptions (iads.h)
description: Provides a direct mechanism to specify and obtain provider-specific options for manipulating an ADSI object.
old-location: adsi\iadsobjectoptions.htm
tech.root: adsi
ms.assetid: 1884efe5-86f5-4579-a25e-2ff9c9a6ec2a
ms.date: 12/05/2018
ms.keywords: IADsObjectOptions, IADsObjectOptions interface [ADSI], IADsObjectOptions interface [ADSI],described, _ds_iadsobjectoptions, adsi.iadsobjectoptions, iads/IADsObjectOptions
f1_keywords:
- iads/IADsObjectOptions
dev_langs:
- c++
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
req.lib: 
req.dll: Activeds.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Activeds.dll
api_name:
- IADsObjectOptions
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IADsObjectOptions interface


## -description


The <b>IADsObjectOptions</b> interface provides a direct mechanism to specify and obtain provider-specific options for manipulating an ADSI object. Typically, the options apply to search operations of the underlying directory store. The supported options are provider-specific.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsObjectOptions</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IADsObjectOptions</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsobjectoptions-getoption">GetOption</a>
</td>
<td align="left" width="63%">
Gets a provider-specific option for a directory object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsobjectoptions-setoption">SetOption</a>
</td>
<td align="left" width="63%">
Sets a provider-specific option for manipulating a directory object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/iads/ne-iads-ads_option_enum">ADS_OPTION_ENUM</a>



<a href="https://docs.microsoft.com/windows/win32/api/iads/ne-iads-ads_security_info_enum">ADS_SECURITY_INFO_ENUM</a>



<a href="https://docs.microsoft.com/windows/desktop/ADSI/fast-binding-option-for-batch-writemodify-operations">Fast Binding Option for Batch Write/Modify Operations</a>



<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsobjectoptions-interface">IADsObjectOptions Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

