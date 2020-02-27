---
UID: NN:cmnquery.IQueryForm
title: IQueryForm (cmnquery.h)
description: Implemented by a query form extension object to allow the form object to add forms and pages to the system-supplied directory service query dialog box.
old-location: ad\iqueryform.htm
tech.root: ad
ms.assetid: fd4f41f0-8aeb-4c83-a079-a5a77685c143
ms.date: 12/05/2018
ms.keywords: IQueryForm, IQueryForm interface [Active Directory], IQueryForm interface [Active Directory],described, _glines_iqueryform, ad.iqueryform, cmnquery/IQueryForm
f1_keywords:
- cmnquery/IQueryForm
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IQueryForm interface


## -description


The <b>IQueryForm</b> interface is implemented by a query form extension object to allow the form object to add forms and pages  to the system-supplied directory service query dialog box.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IQueryForm</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IQueryForm</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/cmnquery/nf-cmnquery-iqueryform-addforms">AddForms</a>
</td>
<td align="left" width="63%">
Add forms.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/cmnquery/nf-cmnquery-iqueryform-addpages">AddPages</a>
</td>
<td align="left" width="63%">
Add pages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/cmnquery/nf-cmnquery-iqueryform-initialize">Initialize</a>
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




<a href="https://docs.microsoft.com/windows/desktop/AD/display-interfaces-in-active-directory-domain-services">Display Interfaces in Active Directory Domain Services</a>
 

 

