---
UID: NF:dsadmin.IDsAdminCreateObj.CreateModal
title: IDsAdminCreateObj::CreateModal (dsadmin.h)
author: windows-sdk-content
description: The IDsAdminCreateObj::CreateModal method displays the object creation wizard and returns the newly created object. The IDsAdminCreateObj::Initialize method must be called before IDsAdminCreateObj::CreateModal can be called.
old-location: ad\idsadmincreateobj_createmodal.htm
tech.root: ad
ms.assetid: 8c157dd8-b569-4171-bd23-b9bce80dbc21
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateModal, CreateModal method [Active Directory], CreateModal method [Active Directory],IDsAdminCreateObj interface, IDsAdminCreateObj interface [Active Directory],CreateModal method, IDsAdminCreateObj.CreateModal, IDsAdminCreateObj::CreateModal, _glines_idsadmincreateobj_createmodal, ad.idsadmincreateobj__createmodal, ad.idsadmincreateobj_createmodal, dsadmin/IDsAdminCreateObj::CreateModal
ms.topic: method
f1_keywords: 
 - "dsadmin/IDsAdminCreateObj.CreateModal"
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
req.lib: 
req.dll: DSAdmin.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DSAdmin.dll
api_name:
 - IDsAdminCreateObj.CreateModal
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDsAdminCreateObj::CreateModal


## -description


The <b>IDsAdminCreateObj::CreateModal</b> method displays the object creation wizard and returns the newly created object. The <a href="https://docs.microsoft.com/windows/desktop/api/dsadmin/nf-dsadmin-idsadmincreateobj-initialize">IDsAdminCreateObj::Initialize</a> method must be called before <b>IDsAdminCreateObj::CreateModal</b> can be called.


## -parameters




### -param hwndParent [in]

Contains the window handle of the owner of the wizard. This value cannot be <b>NULL</b>. Use the result of the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getdesktopwindow">GetDesktopWindow</a> function if no parent window is available.


### -param ppADsObj [out]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iads">IADs</a> interface pointer that receives the newly created object. This parameter receives <b>NULL</b> if the object creation wizard fails or is canceled. The caller must release this interface when it is no longer required. This parameter may be <b>NULL</b> if this object is not required.


## -returns



This method can return one of these values.


Returns an OLE-defined error code or one of the following values.






## -remarks



If the user cancels the object creation wizard, this method returns S_FALSE.  If <i>ppADsObj</i> is not <b>NULL</b>, <i>ppADsObj</i> receives a <b>NULL</b> value. Because of this, the use of the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-succeeded">SUCCEEDED</a> macro to determine if <i>ppADsObj</i> is valid should be avoided. Always test the contents of <i>ppADsObj</i> for a non-<b>NULL</b> value before using the interface pointer.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getdesktopwindow">GetDesktopWindow</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dsadmin/nn-dsadmin-idsadmincreateobj">IDsAdminCreateObj</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dsadmin/nf-dsadmin-idsadmincreateobj-initialize">IDsAdminCreateObj::Initialize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-succeeded">SUCCEEDED</a>
 

 

