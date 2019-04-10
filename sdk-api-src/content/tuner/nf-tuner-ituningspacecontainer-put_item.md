---
UID: NF:tuner.ITuningSpaceContainer.put_Item
title: ITuningSpaceContainer::put_Item (tuner.h)
author: windows-sdk-content
description: The put_Item method saves changes to an existing tuning space in the collection.
old-location: mstv\ituningspacecontainer_put_item.htm
tech.root: mstv
ms.assetid: 44e82ec9-ffd0-4bc9-88da-b6c135cbd98f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITuningSpaceContainer interface [Microsoft TV Technologies],put_Item method, ITuningSpaceContainer.put_Item, ITuningSpaceContainer::put_Item, ITuningSpaceContainerput_Item, mstv.ituningspacecontainer_put_item, put_Item, put_Item method [Microsoft TV Technologies], put_Item method [Microsoft TV Technologies],ITuningSpaceContainer interface, tuner/ITuningSpaceContainer::put_Item
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - tuner.h
api_name:
 - ITuningSpaceContainer.put_Item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITuningSpaceContainer::put_Item


## -description



The <b>put_Item</b> method saves changes to an existing tuning space in the collection.




## -parameters




### -param varIndex [in]

<b>VARIANT</b> that specifies the index of the tuning space.


### -param TuningSpace [in]

Pointer to the <a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace</a> interface of the tuning space.


## -returns



Returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 

If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



An application can retrieve an existing tuning space from the collection, modify its properties by calling <a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace</a> methods, and then call <b>put_Item</b> to save the changes. The unique name property on the tuning space must match the tuning space at the specified index in the collection; otherwise, the method returns E_INVALIDARG.

To add a new tuning space, use the <a href="https://msdn.microsoft.com/9c7faab5-48d4-47fa-be8a-7dafce8504a6">ITuningSpaceContainer::Add</a> method.




## -see-also




<a href="https://msdn.microsoft.com/8f053c53-2a2b-4d98-a510-c516faa21611">ITuningSpaceContainer Interface</a>
 

 

