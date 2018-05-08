---
UID: NF:photoacquire.IPhotoProgressDialog.GetUserInput
title: IPhotoProgressDialog::GetUserInput
author: windows-driver-content
description: Retrieves descriptive information entered by the user, such as the tag name of the images to store.
old-location: picacq\iphotoprogressdialog_getuserinput.htm
old-project: acquisition
ms.assetid: 1f797e68-f87d-4f90-853b-60c6c9309f58
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetUserInput, GetUserInput method [Picture Acquisition], GetUserInput method [Picture Acquisition],IPhotoProgressDialog interface, IPhotoProgressDialog interface [Picture Acquisition],GetUserInput method, IPhotoProgressDialog.GetUserInput, IPhotoProgressDialog::GetUserInput, IPhotoProgressDialogGetUserInput, photoacquire/IPhotoProgressDialog::GetUserInput, picacq.iphotoprogressdialog_getuserinput
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: photoacquire.h
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
req.typenames: USER_INPUT_STRING_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PhotoAcquireUID.lib
-	PhotoAcquireUID.dll
api_name:
-	IPhotoProgressDialog.GetUserInput
product: Windows
targetos: Windows
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPhotoProgressDialog::GetUserInput


## -description



Retrieves descriptive information entered by the user, such as the tag name of the images to store.




## -parameters




### -param riidType [in]

Specifies the interface identifier (ID) of the prompt type. Currently, the only supported value is IID_IUserInputString.


### -param pUnknown [in]

Pointer to an object of the prompt class. Currently, the only supported type is <a href="https://msdn.microsoft.com/f942fefc-2db1-4067-8311-f9ebbaca9d31">IUserInputString</a>.


### -param pPropVarResult [out]

Pointer to a property variant that stores the user input. Must be freed by the caller using <b>ClearPropVariant</b>.


### -param pPropVarDefault [in]

Pointer to a property variant containing the default value to be used if no input is supplied.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The progress dialog has been suppressed

</td>
</tr>
</table>
 




## -remarks



If the progress dialog box has been suppressed in <a href="https://msdn.microsoft.com/1000511f-40a6-4d5e-a55f-97e25f6c1e11">IPhotoAcquire::Acquire</a>, and <a href="https://msdn.microsoft.com/db0d924b-a586-4f81-a367-e8fbdf3e9bd9">IPhotoAcquireProgressCB::GetUserInput</a> is either not implemented, or returns E_NOTIMPL, this method will return S_FALSE, and <i>pPropVarResult</i> will contain the value stored in the optional <i>pPropVarDefault</i> argument.




## -see-also




<a href="https://msdn.microsoft.com/c4fcc470-1b05-4d33-8581-80c6e7488e04">IPhotoAcquireProgressCB Interface</a>



<a href="https://msdn.microsoft.com/a3928874-5a15-43d9-9d9c-8b66478b0597">IPhotoProgressDialog Interface</a>
 

 

