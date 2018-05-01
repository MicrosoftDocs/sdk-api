---
UID: NF:mswmdm.IMDSPDevice3.SetProperty
title: IMDSPDevice3::SetProperty method
author: windows-driver-content
description: The SetProperty method sets a specific device property that is writable.
old-location: wmdm\imdspdevice3_setproperty.htm
old-project: WMDM
ms.assetid: 72bbf8c3-a7e1-4289-b5b0-a57f50d6f46e
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: IMDSPDevice3, IMDSPDevice3 interface [windows Media Device Manager], SetProperty method, IMDSPDevice3::SetProperty, IMDSPDevice3TransferSessionEnd, SetProperty method [windows Media Device Manager], SetProperty method [windows Media Device Manager], IMDSPDevice3 interface, SetProperty,IMDSPDevice3.SetProperty, mswmdm/IMDSPDevice3::SetProperty, wmdm.imdspdevice3_setproperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mssachlp.lib
-	mssachlp.dll
api_name:
-	IMDSPDevice3.SetProperty
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMDSPDevice3::SetProperty method


## -description



The <b>SetProperty</b> method sets a specific device property that is writable.




## -parameters




### -param pwszPropName [in]

Name of device property being set.


### -param pValue [in]

Value of device property being set.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



This method sets the specified device property.

For a list of device property names, see <a href="https://msdn.microsoft.com/870c0e36-aa26-4ab3-b47f-81346d005fa5">Metadata Constants</a>.

This method is similar to the <b>SetMetadata</b> method for storages, but this method can set only one property at a time.




## -see-also




<a href="https://msdn.microsoft.com/919c26f4-6954-462a-8b4a-530e78bb72e6">IMDSPDevice3 Interface</a>



<a href="https://msdn.microsoft.com/e0665ba6-361d-488c-9100-68f39855b736">IMDSPDevice3::GetProperty</a>



<a href="https://msdn.microsoft.com/bfb9a1e4-3cf6-4605-9613-d93f9cce201b">IMDSPStorage3::SetMetadata</a>



<a href="https://msdn.microsoft.com/0f7b3a68-97b3-4470-8ca8-e8eb8a5f83b7">IMDSPStorage4::GetSpecifiedMetadata</a>



<a href="https://msdn.microsoft.com/870c0e36-aa26-4ab3-b47f-81346d005fa5">Metadata Constants</a>
 

 

