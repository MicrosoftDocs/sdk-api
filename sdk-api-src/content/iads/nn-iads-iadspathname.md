---
UID: NN:iads.IADsPathname
title: IADsPathname
author: windows-driver-content
description: Parses the X.500 and Windows path in ADSI.
old-location: adsi\iadspathname.htm
old-project: ADSI
ms.assetid: 9aa26d6c-aa86-4a23-a986-b8cb9057772a
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IADsPathname, IADsPathname interface [ADSI], IADsPathname interface [ADSI],described, Pathname, _ds_iadspathname, adsi.iadspathname, iads/IADsPathname
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
-	IADsPathname
-	Pathname
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsPathname interface


## -description


The <b>IADsPathname</b> interface parses the X.500 and Windows path in ADSI.

The <b>IADsPathname</b> interface can be used to:
<ul>
<li>Set and get paths of ADSI objects in different formats.</li>
<li>Extract or add each element for a given ADsPath.</li>
<li>Construct ADsPaths to be used in queries of directory objects.</li>
</ul>The <b>IADsPathname</b> interface is implemented on a <b>Pathname</b> object. You must instantiate the <b>Pathname</b> object to use the methods defined in the <b>IADsPathname</b> interface. This requirement is similar to calling the  <a href="_com_cocreateinstance">CoCreateInstance()</a> function in C++.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IADsPathname *pPathname=NULL;
HRESULT hr;
 
hr = CoCreateInstance(CLSID_Pathname,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IADsPathname,
                      (void**)&amp;pPathname);</pre>
</td>
</tr>
</table></span></div>You can also invoke the <b>New</b> operator in Visual Basic:
<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim path As New Pathname</pre>
</td>
</tr>
</table></span></div>Or use the <b>CreateObject</b> function in VBScript, supplying "Pathname" as the ProgID.
<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim path
Set path = CreateObject("Pathname")</pre>
</td>
</tr>
</table></span></div>The <b>IADsPathname</b> interface uses two enumeration types:  <a href="https://msdn.microsoft.com/fbf7de54-3ea7-4d66-ad56-21cae1e28c07">ADS_SETTYPE_ENUM</a>, and  <a href="https://msdn.microsoft.com/d0c94f30-6b8c-4c7a-bb74-205b2b658dbb">ADS_FORMAT_ENUM</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsPathname</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IADsPathname</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IADsPathname</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f29f11f-965e-4556-af74-2bc06588410f">AddLeafElement</a>
</td>
<td align="left" width="63%">
Adds an element to the end of the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00c4a0b8-4961-4ceb-86fe-5cdc4e0a45c0">CopyPath</a>
</td>
<td align="left" width="63%">
Generates an object with the same path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6fc027c7-6645-4596-b438-99795f9e66fc">GetElement</a>
</td>
<td align="left" width="63%">
Gets elements stored in the object with its index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a61702bd-26a8-4bd9-96c1-82a59dad7ead">GetEscapedElement</a>
</td>
<td align="left" width="63%">
Escapes an RDN string and returns the output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad6518c8-d379-4062-888f-cbf84995fc39">GetNumElements</a>
</td>
<td align="left" width="63%">
Gets the number of elements in the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90085c75-0a38-43e8-932e-2b89d167cfa5">RemoveLeafElement</a>
</td>
<td align="left" width="63%">
Removes the last element from the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c34f2a5e-5faf-45bf-acc6-8db5fc8bf5fa">Retrieve</a>
</td>
<td align="left" width="63%">
Retrieves an object path with an <a href="https://msdn.microsoft.com/d0c94f30-6b8c-4c7a-bb74-205b2b658dbb">ADS_FORMAT_ENUM</a> type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff544503">Set</a>
</td>
<td align="left" width="63%">
Sets an object path with an <a href="https://msdn.microsoft.com/fbf7de54-3ea7-4d66-ad56-21cae1e28c07">ADS_SETTYPE_ENUM</a> option.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d975482-74f6-4ffa-a243-baa5f6a8d200">SetDisplayType</a>
</td>
<td align="left" width="63%">
Specifies how a path is to be displayed.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsPathname</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/007ec617-cff2-492a-a62c-50d65fefcd3b">EscapedMode</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves the mode for escaping a path.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d0c94f30-6b8c-4c7a-bb74-205b2b658dbb">ADS_FORMAT_ENUM</a>



<a href="https://msdn.microsoft.com/fbf7de54-3ea7-4d66-ad56-21cae1e28c07">ADS_SETTYPE_ENUM</a>



<a href="_com_cocreateinstance">CoCreateInstance()</a>



<a href="https://msdn.microsoft.com/007ec617-cff2-492a-a62c-50d65fefcd3b">IADsPathname Property
    Methods</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

