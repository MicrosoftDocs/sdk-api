---
UID: NN:fsrmreports.IFsrmPropertyCondition
title: IFsrmPropertyCondition (fsrmreports.h)
description: Defines a property condition that the file management job uses to determine if the file is expired.
old-location: fsrm\ifsrmpropertycondition.htm
tech.root: fsrm
ms.assetid: 5c50b86b-f166-459e-92ce-63faa374c407
ms.date: 12/05/2018
ms.keywords: IFsrmPropertyCondition, IFsrmPropertyCondition interface [File Server Resource Manager], IFsrmPropertyCondition interface [File Server Resource Manager],described, fs.ifsrmpropertycondition, fsrm.ifsrmpropertycondition, fsrm/IFsrmPropertyCondition
ms.topic: interface
f1_keywords:
- fsrmreports/IFsrmPropertyCondition
dev_langs:
- c++
req.header: fsrmreports.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
req.dll: SrmSvc.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- SrmSvc.dll
api_name:
- IFsrmPropertyCondition
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmPropertyCondition interface


## -description


Defines a property condition that the file management job uses to determine if the file is expired.

To create this interface, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-createpropertycondition">IFsrmFileManagementJob::CreatePropertyCondition</a>   method.

The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_propertyconditions">IFsrmFileManagementJob.PropertyConditions</a> property contains a collection of these interfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmPropertyCondition</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmPropertyCondition</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFsrmPropertyCondition</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmpropertycondition-delete">Delete</a>
</td>
<td align="left" width="63%">
Removes this property condition from the collection of property conditions specified for the file management job.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmPropertyCondition</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

[Name](/windows/win32/api/fsrmreports/nf-fsrmreports-ifsrmpropertycondition-get_name)a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The name of the classification property whose value you want to compare to the property condition's value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/ifsrmpropertycondition-type">Type</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The comparison operator used to determine whether property condition is met.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

[Value](/windows/win32/api/fsrmreports/nf-fsrmreports-ifsrmpropertycondition-get_value)a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The property condition's value.

</td>
</tr>
</table> 


## -remarks



The property condition specifies the classification property in the file to test. When the file management job runs, it gets the value of the classification property and uses the comparison operator to compare the value of the specified classification property (see the [Value](/windows/win32/api/fsrmreports/nf-fsrmreports-ifsrmpropertycondition-get_value)a> property). If this condition  and all the other specified conditions for the job are met, FSRM can expire the file or call the custom action if it is defined.



