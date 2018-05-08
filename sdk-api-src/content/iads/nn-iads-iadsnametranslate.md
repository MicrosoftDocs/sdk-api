---
UID: NN:iads.IADsNameTranslate
title: IADsNameTranslate
author: windows-driver-content
description: The IADsNameTranslate interface translates distinguished names (DNs) among various formats as defined in the ADS_NAME_TYPE_ENUM enumeration. The feature is available to objects in Active Directory.
old-location: adsi\iadsnametranslate.htm
old-project: ADSI
ms.assetid: 3d8baeb1-0edc-4648-8691-6ea4dcfd8f62
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IADsNameTranslate, IADsNameTranslate interface [ADSI], IADsNameTranslate interface [ADSI],described, NameTranslate, _ds_iadsnametranslate, adsi.iadsnametranslate, iads/IADsNameTranslate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: iads.h
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
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Activeds.dll
api_name:
-	IADsNameTranslate
-	NameTranslate
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsNameTranslate interface


## -description


The <b>IADsNameTranslate</b>
  interface translates distinguished names (DNs) among various
  formats as defined in the 
   <a href="https://msdn.microsoft.com/8c5e8f2a-e805-463e-9583-96732d70b209">ADS_NAME_TYPE_ENUM</a> enumeration.
  The feature is available to objects in Active Directory.

Name
  translations are performed on the directory server. To translate a DN, communicate with the server by means of an <b>IADsNameTranslate</b> object, and specify which object is of interest
  and what format is desired. The following is the general process for using the
  <b>IADsNameTranslate</b> interface.

First, create an instance of the <b>IADsNameTranslate</b> object.

Second, initialize the <b>IADsNameTranslate</b>
    object by specifying the directory server using the  
     <a href="https://msdn.microsoft.com/dad31301-b18b-44ec-b32f-93d0bb5b6189">IADsNameTranslate::Init</a>
    or 
     <a href="https://msdn.microsoft.com/169e1e0d-26c0-484d-b461-8817d37d17b8">IADsNameTranslate::InitEx</a> methods.

Third, set the directory object on the server by specifying the name with the <a href="https://msdn.microsoft.com/1c126333-3d5c-4ba3-8c66-de778e26488f">IADsNameTranslate::Set</a> method and the format with the <a href="https://msdn.microsoft.com/e8a5014e-d848-46b7-a336-7801ff1f6b08">IADsNameTranslate::SetEx</a> method.

Fourth, retrieve the object name in the specified format with the <a href="https://msdn.microsoft.com/6c8246a9-657e-4db1-ae8f-d9c0a2d41397">IADsNameTranslate::Get</a>
    or 
     <a href="https://msdn.microsoft.com/01c4fc79-ed5b-4a24-9b97-25b4095a9c8f">IADsNameTranslate::GetEx</a> method.

The following code example shows how to create an <b>IADsNameTranslate</b> object in Visual C++, Visual Basic, and
  VBScript/Active Server Pages.
<div class="alert"><b>Note</b>  The format elements as defined in the <a href="https://msdn.microsoft.com/8c5e8f2a-e805-463e-9583-96732d70b209">ADS_NAME_TYPE_ENUM</a> enumeration and used
  by <b>IADsNameTranslate</b> are not equivalent and are 
  non-interchangeable with the format elements used by the
  <a href="https://msdn.microsoft.com/f812a001-5aab-4c62-87bd-54f95792e271">DsCrackName</a> function. Do not confuse the proper use of these similarly named but non-interchangeable element
  formats.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsNameTranslate</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IADsNameTranslate</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IADsNameTranslate</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj983411">Get</a>
</td>
<td align="left" width="63%">
Gets the object name, set by <a href="https://msdn.microsoft.com/library/windows/hardware/ff544503">Set</a>, in a specified format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01c4fc79-ed5b-4a24-9b97-25b4095a9c8f">GetEx</a>
</td>
<td align="left" width="63%">
Gets the names of the objects, set by <a href="https://msdn.microsoft.com/e8a5014e-d848-46b7-a336-7801ff1f6b08">SetEx</a>, in a specified format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541624">Init</a>
</td>
<td align="left" width="63%">
Initializes the <b>IADsNameTranslate</b>
    object with default credentials.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/169e1e0d-26c0-484d-b461-8817d37d17b8">InitEx</a>
</td>
<td align="left" width="63%">
Initializes the <b>IADsNameTranslate</b>
    object with specified credentials.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff544503">Set</a>
</td>
<td align="left" width="63%">
Specifies the object name to translate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e8a5014e-d848-46b7-a336-7801ff1f6b08">SetEx</a>
</td>
<td align="left" width="63%">
Sets the names of multiple objects at the same time.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsNameTranslate</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7c44fe9b-16a5-4bd5-a80b-8f3dcfec20cc">ChaseReferral</a>


</td>
<td align="left" width="10%">
Write-only

</td>
<td align="left" width="63%">
Toggles referral chasing ON or OFF.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/8c5e8f2a-e805-463e-9583-96732d70b209">ADS_NAME_TYPE_ENUM</a>



<a href="_com_cocreateinstance">CoCreateInstance</a>



<a href="https://msdn.microsoft.com/7c44fe9b-16a5-4bd5-a80b-8f3dcfec20cc">IADsNameTranslate
    Property Methods</a>



<a href="https://msdn.microsoft.com/c5c6e821-f19b-4269-81de-34c79dd2731f">IADsNameTranslate Interface</a>



<a href="https://msdn.microsoft.com/6c8246a9-657e-4db1-ae8f-d9c0a2d41397">IADsNameTranslate::Get</a>



<a href="https://msdn.microsoft.com/01c4fc79-ed5b-4a24-9b97-25b4095a9c8f">IADsNameTranslate::GetEx</a>



<a href="https://msdn.microsoft.com/dad31301-b18b-44ec-b32f-93d0bb5b6189">IADsNameTranslate::Init</a>



<a href="https://msdn.microsoft.com/169e1e0d-26c0-484d-b461-8817d37d17b8">IADsNameTranslate::InitEx</a>



<a href="https://msdn.microsoft.com/1c126333-3d5c-4ba3-8c66-de778e26488f">IADsNameTranslate::Set</a>



<a href="https://msdn.microsoft.com/e8a5014e-d848-46b7-a336-7801ff1f6b08">IADsNameTranslate::SetEx</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

