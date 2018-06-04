---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IPublishingWizard::GetTransferManifest


## -description


Gets a transfer manifest for a file transfer operation performed by a publishing wizard, such as the Online Print Wizard or the Add Network Place Wizard.  

            
<div class="alert"><b>Note</b>  This method is deprecated for Windows Vista, as it is not supported for Online Print Wizard or Add Network Place Wizard.</div><div> </div>

## -parameters




### -param phrFromTransfer [out]

Type: <b>HRESULT*</b>

A pointer to a variable of type <b>HRESULT</b> that, when this method returns, is set to S_OK if the transfer operation was successful, S_FALSE if the transfer has not yet begun, or a standard error value if the transfer has failed or has been canceled. This value can be <b>NULL</b> if you do not require this information.


### -param pdocManifest [out]

Type: <b>IXMLDOMDocument**</b>

Address of an <a href="7d0088e0-c309-4e57-9533-6700f80074b3">IXMLDOMDocument interface</a> pointer that, when this method returns, points to the <b>IXMLDOMDocument interface</b> object that represents the manifest. This value can be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if the manifest is successfully retrieved or a standard COM error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The transfer manifest has not yet been created.

</td>
</tr>
</table>
 




## -remarks



The transfer manifest is not created until the wizard is actually displayed. For information on displaying a publishing wizard, see the <a href="https://msdn.microsoft.com/634dcc04-e2ed-4cde-bb4d-d2e8bcf5ab94">IPublishingWizard</a> topic.




## -see-also




<a href="https://msdn.microsoft.com/634dcc04-e2ed-4cde-bb4d-d2e8bcf5ab94">IPublishingWizard</a>



<a href="https://msdn.microsoft.com/488b6fc9-ff85-4860-9cd5-61d5de7e15e8">Transfer Manifest Schema</a>



<a href="https://msdn.microsoft.com/b7bb541c-3bf4-4aab-ac70-c006517e772e">Using the Transfer Manifest</a>
 

 

