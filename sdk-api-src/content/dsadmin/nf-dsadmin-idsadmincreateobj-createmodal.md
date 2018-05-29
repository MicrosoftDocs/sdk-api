---
UID: NF:dsadmin.IDsAdminCreateObj.CreateModal
title: IDsAdminCreateObj::CreateModal
author: windows-sdk-content
description: The IDsAdminCreateObj::CreateModal method displays the object creation wizard and returns the newly created object. The IDsAdminCreateObj::Initialize method must be called before IDsAdminCreateObj::CreateModal can be called.
old-location: ad\idsadmincreateobj_createmodal.htm
old-project: AD
ms.assetid: 8c157dd8-b569-4171-bd23-b9bce80dbc21
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: CreateModal, CreateModal method [Active Directory], CreateModal method [Active Directory],IDsAdminCreateObj interface, IDsAdminCreateObj interface [Active Directory],CreateModal method, IDsAdminCreateObj.CreateModal, IDsAdminCreateObj::CreateModal, _glines_idsadmincreateobj_createmodal, ad.idsadmincreateobj__createmodal, ad.idsadmincreateobj_createmodal, dsadmin/IDsAdminCreateObj::CreateModal
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dsadmin.h
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
req.typenames: DRT_ADDRESS_LIST, *PDRT_ADDRESS_LIST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DSAdmin.dll
api_name:
-	IDsAdminCreateObj.CreateModal
product: Windows
targetos: Windows
req.lib: 
req.dll: DSAdmin.dll
req.irql: 
---

# IDsAdminCreateObj::CreateModal


## -description


The <b>IDsAdminCreateObj::CreateModal</b> method displays the object creation wizard and returns the newly created object. The <a href="https://msdn.microsoft.com/811863e7-25d2-48d0-bf97-61b49a224c98">IDsAdminCreateObj::Initialize</a> method must be called before <b>IDsAdminCreateObj::CreateModal</b> can be called.


## -parameters




### -param hwndParent [in]

Contains the window handle of the owner of the wizard. This value cannot be <b>NULL</b>. Use the result of the <a href="_win32_getdesktopwindow_cpp">GetDesktopWindow</a> function if no parent window is available.


### -param ppADsObj [out]

Pointer to an <a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a> interface pointer that receives the newly created object. This parameter receives <b>NULL</b> if the object creation wizard fails or is canceled. The caller must release this interface when it is no longer required. This parameter may be <b>NULL</b> if this object is not required.


## -returns



This method can return one of these values.


Returns an OLE-defined error code or one of the following values.






## -remarks



If the user cancels the object creation wizard, this method returns S_FALSE.  If <i>ppADsObj</i> is not <b>NULL</b>, <i>ppADsObj</i> receives a <b>NULL</b> value. Because of this, the use of the <a href="_com_succeeded">SUCCEEDED</a> macro to determine if <i>ppADsObj</i> is valid should be avoided. Always test the contents of <i>ppADsObj</i> for a non-<b>NULL</b> value before using the interface pointer.




## -see-also




<a href="_win32_getdesktopwindow_cpp">GetDesktopWindow</a>



<a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>



<a href="https://msdn.microsoft.com/93673b29-744a-4100-86b7-8a2eec861c47">IDsAdminCreateObj</a>



<a href="https://msdn.microsoft.com/811863e7-25d2-48d0-bf97-61b49a224c98">IDsAdminCreateObj::Initialize</a>



<a href="_com_succeeded">SUCCEEDED</a>
 

 

