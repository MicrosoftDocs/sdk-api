---
UID: NN:xpsobjectmodel.IXpsOMCoreProperties
title: IXpsOMCoreProperties
author: windows-sdk-content
description: This interface provides access to the metadata that is stored in the Core Properties part of the XPS document.
old-location: xps\ixpsomcoreproperties.htm
old-project: printdocs
ms.assetid: 705ec9c7-5aa9-4fc5-ad2c-441cb545d056
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IXpsOMCoreProperties, IXpsOMCoreProperties interface [XPS Documents and Packaging], IXpsOMCoreProperties interface [XPS Documents and Packaging],described, xps.ixpsomcoreproperties, xpsobjectmodel/IXpsOMCoreProperties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: XPS_INTERLEAVING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMCoreProperties
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMCoreProperties interface


## -description


This interface provides access to the metadata that is stored in the Core Properties part of the XPS document.

The contents of the Core Properties part are described in  the 1st edition, Part 2, "Open Packaging Conventions," of <a href="http://go.microsoft.com/fwlink/p/?linkid=123375">Standard ECMA-376, Office Open XML File Formats</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMCoreProperties</b> interface inherits from <a href="https://msdn.microsoft.com/71cd0155-6c95-42ca-bfc3-dffd43d95dc9">IXpsOMPart</a>. <b>IXpsOMCoreProperties</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMCoreProperties</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Makes a deep copy of the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97b1b0ca-a2e7-4835-aece-c2cc23481530">GetCategory</a>
</td>
<td align="left" width="63%">

              Gets the <b>category</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e058e8d-ace6-4892-87c1-07e28ff24462">GetContentStatus</a>
</td>
<td align="left" width="63%">

              Gets the <b>contentStatus</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a032cd7-90b3-427c-bbdf-2265f15c6f23">GetContentType</a>
</td>
<td align="left" width="63%">

              Gets the <b>contentType</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ee96d96-bd66-4738-bfae-fbbc98ba8621">GetCreated</a>
</td>
<td align="left" width="63%">

              Gets the <b>created</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35d7a3ad-e1f7-49bf-ad30-d577cc9d4731">GetCreator</a>
</td>
<td align="left" width="63%">

              Gets the <b>creator</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546575">GetDescription</a>
</td>
<td align="left" width="63%">

              Gets the <b>description</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a397fba0-4e73-4f5b-b292-529a222c2501">GetIdentifier</a>
</td>
<td align="left" width="63%">

              Gets the <b>identifier</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0bac4c7-5bb6-4a9d-8f16-db97e7efee5a">GetKeywords</a>
</td>
<td align="left" width="63%">

              Gets the <b>keywords</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a35185a-0dbc-48bb-8ae1-53fafa197bb7">GetLanguage</a>
</td>
<td align="left" width="63%">

              Gets the <b>language</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3e68656-ae4d-45f4-bb2a-3c4c5cecbbae">GetLastModifiedBy</a>
</td>
<td align="left" width="63%">

              Gets the <b>lastModifiedBy</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7e4b994-ec4f-415d-a340-813f00adba19">GetLastPrinted</a>
</td>
<td align="left" width="63%">

              Gets the <b>lastPrinted</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/364beb9d-01e7-477c-92b2-f2fdb19a87f9">GetModified</a>
</td>
<td align="left" width="63%">

              Gets the <b>modified</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3b2b9a7-7498-48a1-9d1f-eb954dc5576c">GetOwner</a>
</td>
<td align="left" width="63%">

              Gets a pointer to the <a href="https://msdn.microsoft.com/7b0a36d6-1af1-4c2c-af14-d6139e9115c3">IXpsOMPackage</a> interface that contains the core properties.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7143e4e7-c5e3-41f8-84d8-64fa3008ccc8">GetRevision</a>
</td>
<td align="left" width="63%">

              Gets the <b>revision</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80499d81-4adc-402c-ab72-4ebc77eefaea">GetSubject</a>
</td>
<td align="left" width="63%">

              Gets the <b>subject</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32551dd2-2d6e-4aaa-864b-4c922a90fc27">GetTitle</a>
</td>
<td align="left" width="63%">

              Gets the <b>title</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0a693e5-fd98-47c0-aaf7-f8461169a01c">GetVersion</a>
</td>
<td align="left" width="63%">

              Gets the <b>version</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c194731-0992-47c3-b069-fa9e1d16944b">SetCategory</a>
</td>
<td align="left" width="63%">

              Sets the <b>category</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f500407d-3eb4-4bf1-88ef-8f6bd2bcf472">SetContentStatus</a>
</td>
<td align="left" width="63%">

              Sets the <b>contentStatus</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97ddb1a2-67b2-4891-86b6-bdd38e609229">SetContentType</a>
</td>
<td align="left" width="63%">

              Sets the <b>contentType</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a71d338-a34e-40df-ade0-130cd8e0a176">SetCreated</a>
</td>
<td align="left" width="63%">

              Sets the <b>created</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83dd62df-71e1-44a6-bf38-461b7e26e54e">SetCreator</a>
</td>
<td align="left" width="63%">

              Sets the <b>creator</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5be76080-0f85-4937-913c-2037740a3e9d">SetDescription</a>
</td>
<td align="left" width="63%">

              Sets the <b>description</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ad5a359-77f6-4b11-9c1c-2e4094be65d0">SetIdentifier</a>
</td>
<td align="left" width="63%">

              Sets the <b>identifier</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d96a85d2-dfbf-4589-9c3f-7505715ec6ce">SetKeywords</a>
</td>
<td align="left" width="63%">

              Sets the <b>keywords</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e17901e8-9adb-488e-9c8d-6fa1351520ac">SetLanguage</a>
</td>
<td align="left" width="63%">

              Sets the <b>language</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c19e7c8-d790-42b8-a0c4-bfd95c7de2c5">SetLastModifiedBy</a>
</td>
<td align="left" width="63%">

              Sets the <b>lastModifiedBy</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b1cf459-b140-4793-a9e0-4153a00b9bc2">SetLastPrinted</a>
</td>
<td align="left" width="63%">

              Sets the <b>lastPrinted</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/172f49b9-850d-46f0-bed1-678a070a7ae8">SetModified</a>
</td>
<td align="left" width="63%">

              Sets the <b>modified</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e2ef3b4-64dd-402e-a282-0ed01e588337">SetRevision</a>
</td>
<td align="left" width="63%">

              Sets the <b>revision</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa194dd0-3293-4c09-84ae-516478862f4c">SetSubject</a>
</td>
<td align="left" width="63%">

              Sets the <b>subject</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55562670-576f-483d-abcf-f69ce279245d">SetTitle</a>
</td>
<td align="left" width="63%">

              Sets the <b>title</b> property.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1058f228-8b81-4590-b0af-08abe16a1510">SetVersion</a>
</td>
<td align="left" width="63%">

              Sets the <b>version</b> property.
            

</td>
</tr>
</table> 


## -remarks



The meaning and use of these properties is determined by the user or context.




## -see-also




<a href="https://msdn.microsoft.com/b7146f0c-e397-45cb-9eb0-e03b3ac0e905">IXpsOMObjectFactory::CreateCoreProperties</a>



<a href="https://msdn.microsoft.com/71cd0155-6c95-42ca-bfc3-dffd43d95dc9">IXpsOMPart</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">Standard ECMA-376, Office Open XML File Formats</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

