---
UID: NF:msdrm.DRMSetNameAndDescription
title: DRMSetNameAndDescription function
author: windows-sdk-content
description: Allows an application to specify names and descriptions of the license in multiple (human) languages.
old-location: rm\drmsetnameanddescription.htm
tech.root: AdRms_Sdk
ms.assetid: c5dc8aa8-f45b-4b8a-bd83-0661db424303
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DRMSetNameAndDescription, DRMSetNameAndDescription function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMSetNameAndDescription, rm.drmsetnameanddescription
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: msdrm.h
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
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMSetNameAndDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMSetNameAndDescription function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMSetNameAndDescription</b> function allows an application to specify names and descriptions of the license in multiple (human) languages.


## -parameters




### -param hIssuanceLicense [in]

A handle to an issuance license.


### -param fDelete [in]

Flag indicating whether the existing item should be deleted:  <b>TRUE</b> indicates it should be deleted; <b>FALSE</b> indicates it should be added.


### -param lcid [in]

A locale ID for this name and description. If <i>lcid</i> is given as <b>NULL</b> or zero, the name and description given become the default license name and description. There may be only one name and description for any LCID (locale identifier).


### -param wszName [in]

A license name, in the language specified by this locale.


### -param wszDescription [in]

An optional license description, in the language specified by this locale.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



This function allows a license to be distributed internationally. A consuming application can display the localized name and description of the license.

<div class="alert"><b>Note</b>  To set a default language for Name and Description, you can set the locale ID to 0. Take note that this is supported only for templates and licenses created programmatically on the client. AD RMS server administration does not support setting a default language for Name and Description.  For more information about creating an issuance license programmatically, see   <a href="https://msdn.microsoft.com/495024be-5d97-4869-99f7-b68efb9e8039">Creating an Issuance License</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/9e04ee69-bfec-456a-99ca-93e3158aeef9">DRMGetNameAndDescription</a>
 

 

