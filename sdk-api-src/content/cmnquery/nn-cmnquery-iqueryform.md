---
UID: NN:cmnquery.IQueryForm
title: IQueryForm
author: windows-sdk-content
description: Implemented by a query form extension object to allow the form object to add forms and pages to the system-supplied directory service query dialog box.
old-location: ad\iqueryform.htm
tech.root: ad
ms.assetid: fd4f41f0-8aeb-4c83-a079-a5a77685c143
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IQueryForm, IQueryForm interface [Active Directory], IQueryForm interface [Active Directory],described, _glines_iqueryform, ad.iqueryform, cmnquery/IQueryForm
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: cmnquery.h
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
req.lib: Uuid.lib
req.dll: Dsquery.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dsquery.dll
api_name:
 - IQueryForm
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IQueryForm interface


## -description


The <b>IQueryForm</b> interface is implemented by a query form extension object to allow the form object to add forms and pages  to the system-supplied directory service query dialog box.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IQueryForm</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IQueryForm</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IQueryForm</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fadaa7e6-ccf2-42cd-a26e-19db107ce56c">AddForms</a>
</td>
<td align="left" width="63%">
Add forms.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/797496fd-67db-4ec2-beec-224664d5d330">AddPages</a>
</td>
<td align="left" width="63%">
Add pages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1250c69-f29b-44f1-b123-13818d26e322">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the query form  object.

</td>
</tr>
</table> 


## -remarks



A query form extension object must be registered in the Windows registry to be available to the query handler. This is accomplished by adding the following registry key.


<pre xml:space="preserve"><b>HKEY_CLASSES_ROOT</b>
   <b>CLSID</b>
      <i>&lt;query handler CLSID&gt;</i>
         <b>Forms</b>
            <i>&lt;name of query form extension&gt;</i></pre>


The <i>&lt;query handler CLSID&gt;</i> key is the class identifier of the form handler. The <i>&lt;name of query form extension&gt;</i> key is the unique name of the query form extension. This name must be unique within the <b>Forms</b> key. It is suggested that the string form of the class identifier of the query form extension be used for the name.

The following list lists the registry entries under the above key.

<table>
<tr>
<th>Registry Entry</th>
<th>Description</th>
</tr>
<tr>
<td><b>CLSID</b></td>
<td>
A string value that contains the class identifier of the object that implements <b>IQueryForm</b>.

</td>
</tr>
<tr>
<td><b>Flags</b></td>
<td>
A numeric value that contains a set of flags that define the behavior of the form. This can be zero or a combination of one or more of the following values.



<dl>
<dt><a id="QUERYFORM_CHANGESFORMLIST"></a><a id="queryform_changesformlist"></a><b>QUERYFORM_CHANGESFORMLIST</b></dt>
<dd>
The form should be visible in the normal form list.

</dd>
<dt><a id="QUERYFORM_CHANGESOPTFORMLIST"></a><a id="queryform_changesoptformlist"></a><b>QUERYFORM_CHANGESOPTFORMLIST</b></dt>
<dd>
The form should be visible in the optional form list.

</dd>
</dl>
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f53d4425-5496-45f8-a09b-f163b63a29c8">Display Interfaces in Active Directory Domain Services</a>
 

 

