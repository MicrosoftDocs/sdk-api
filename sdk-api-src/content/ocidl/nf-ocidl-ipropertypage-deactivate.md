---
UID: NF:ocidl.IPropertyPage.Deactivate
title: IPropertyPage::Deactivate (ocidl.h)
author: windows-sdk-content
description: Destroys the window created in IPropertyPage::Activate.
old-location: com\ipropertypage_deactivate.htm
tech.root: com
ms.assetid: 545f7c3d-3c6f-42c2-b472-3da3bc184200
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Deactivate, Deactivate method [COM], Deactivate method [COM],IPropertyPage interface, IPropertyPage interface [COM],Deactivate method, IPropertyPage.Deactivate, IPropertyPage::Deactivate, _ctrl_ipropertypage_deactivate, com.ipropertypage_deactivate, ocidl/IPropertyPage::Deactivate
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - OCIdl.h
api_name:
 - IPropertyPage.Deactivate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyPage::Deactivate


## -description


Destroys the window created in <a href="https://msdn.microsoft.com/4756d06d-0ffc-4214-9c2b-d9cb169b4337">IPropertyPage::Activate</a>.


## -parameters






## -returns



This method can return the standard return values E_UNEXPECTED and S_OK.




## -remarks



<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
It is important that property pages not keep the dialog box around as an optimization. In a property sheet with many property pages, memory consumption would become excessive if all property pages kept their dialog boxes created at all times. Destroying the dialog box prevents excessive memory consumption due to a very large number of created controls in the dialog boxes. If the frame wishes to keep pages alive while they are not visible, it can use <a href="https://msdn.microsoft.com/f89aa820-a3d3-4a41-b2b2-9ee48354fbeb">IPropertyPage::Show</a> for that purpose. The decision is ultimately left to the frame.

E_NOTIMPL is not a valid return value.




## -see-also




<a href="https://msdn.microsoft.com/ad2cb3ae-dd24-4774-95bd-f5a0773c68b1">IPropertyPage</a>
 

 

