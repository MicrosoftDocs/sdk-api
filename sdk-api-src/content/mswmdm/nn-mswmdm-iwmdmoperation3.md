---
UID: NN:mswmdm.IWMDMOperation3
title: IWMDMOperation3 (mswmdm.h)
author: windows-sdk-content
description: The optional, application-implemented IWMDMOperation3 interface extends IWMDMOperation by providing a new method for transferring data unencrypted for added efficiency.
old-location: wmdm\iwmdmoperation3.htm
tech.root: WMDM
ms.assetid: 5ab4fdd2-d0bf-4e2c-b529-331ffa4c8403
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMDMOperation3, IWMDMOperation3 interface [windows Media Device Manager], IWMDMOperation3 interface [windows Media Device Manager],described, IWMDMOperation3Interface, mswmdm/IWMDMOperation3, wmdm.iwmdmoperation3
ms.topic: interface
f1_keywords: 
 - "mswmdm/IWMDMOperation3"
req.header: mswmdm.h
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
 - mswmdm.h
api_name:
 - IWMDMOperation3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDMOperation3 interface


## -description



The optional, application-implemented <b>IWMDMOperation3</b> interface extends <b>IWMDMOperation</b> by providing a new method for transferring data unencrypted for added efficiency.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMOperation3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation">IWMDMOperation</a>. <b>IWMDMOperation3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMOperation3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel">TransferObjectDataOnClearChannel</a>
</td>
<td align="left" width="63%">
Transfers a block of data to or from the device more efficiently than <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata">IWMDMOperation::TransferObjectData</a>.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMDM/handling-file-transfers-manually">Handling File Transfers Manually</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation">IWMDMOperation Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation2">IWMDMOperation2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
 

 

