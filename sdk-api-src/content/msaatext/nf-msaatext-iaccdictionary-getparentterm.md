---
UID: NF:msaatext.IAccDictionary.GetParentTerm
title: IAccDictionary::GetParentTerm
author: windows-sdk-content
description: Clients call the IAccDictionary::GetParentTerm method to navigate through the object hierarchy tree. This method returns the parent object of a specified property.
old-location: winauto\iaccdictionary_iaccdictionary__getparentterm.htm
old-project: WinAuto
ms.assetid: 202058e8-50c2-4366-9bb6-bbc46dc5ea3f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetParentTerm, GetParentTerm method [Windows Accessibility], GetParentTerm method [Windows Accessibility],IAccDictionary interface, IAccDictionary interface [Windows Accessibility],GetParentTerm method, IAccDictionary.GetParentTerm, IAccDictionary::GetParentTerm, _msaa_IAccDictionary_GetParentTerm, msaa.iaccdictionary_iaccdictionary__getparentterm, msaatext/IAccDictionary::GetParentTerm, winauto.iaccdictionary_iaccdictionary__getparentterm
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msaatext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: SSTP_CONFIG_PARAMS, *PSSTP_CONFIG_PARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msaatext.dll
api_name:
 - IAccDictionary.GetParentTerm
product: Windows
targetos: Windows
req.lib: 
req.dll: Msaatext.dll
req.irql: 
req.product: GDI+ 1.1
---

# IAccDictionary::GetParentTerm


## -description


Clients call the <b>IAccDictionary::GetParentTerm</b> method to navigate through the object hierarchy tree. This method returns the parent object of a specified property.
<div class="alert"><b>Note</b>  Active Accessibility Text Services is deprecated. Please see     
<a href="http://go.microsoft.com/fwlink/p/?linkid=131573">Microsoft Windows Text Services Framework</a>for more information on advanced text input and natural language technologies.
		</div><div> </div>

## -parameters




### -param Term [in]

Type: <b>REFGUID</b>

A GUID for a property.


### -param pParentTerm [out]

Type: <b>GUID*</b>

The parent of the property specified in the <i>Term</i> parameter.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK.




## -remarks



If there is not a parent term for <i>Term</i>, then <i>pParentTerm</i> will point to GUID_NULL.



