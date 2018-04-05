---
UID: NF:fsrmreports.IFsrmReportManager.SetReportSizeLimit
title: IFsrmReportManager::SetReportSizeLimit method
author: windows-driver-content
description: Sets the current value of the specified report size limit.
old-location: fsrm\ifsrmreportmanager_setreportsizelimit.htm
old-project: Fsrm
ms.assetid: 7d5a73ab-eccb-42e5-8796-d2986deccd34
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: FsrmReportManager class [File Server Resource Manager], SetReportSizeLimit method, IFsrmReportManager, IFsrmReportManager interface [File Server Resource Manager], SetReportSizeLimit method, IFsrmReportManager::SetReportSizeLimit, SetReportSizeLimit method [File Server Resource Manager], SetReportSizeLimit method [File Server Resource Manager], FsrmReportManager class, SetReportSizeLimit method [File Server Resource Manager], IFsrmReportManager interface, SetReportSizeLimit,IFsrmReportManager.SetReportSizeLimit, fs.ifsrmreportmanager_setreportsizelimit, fsrm.ifsrmreportmanager_setreportsizelimit, fsrmreports/IFsrmReportManager::SetReportSizeLimit
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: fsrmreports.h
req.include-header: FsrmReports.h, FsrmTlb.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: FsrmTemplateApplyOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmReportManager.SetReportSizeLimit
-	FsrmReportManager.SetReportSizeLimit
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmReportManager::SetReportSizeLimit method


## -description


Sets the current value of the specified report size limit.


## -parameters




### -param limit [in]

Identifies the limit which is used to limit the files listed in a report. For possible values, see the 
      <a href="https://msdn.microsoft.com/225c583c-679c-43b4-85f4-3f2294fa7bc3">FsrmReportLimit</a> enumeration.


### -param limitValue [in]

The limit. Must be greater than zero. You can specify the variant as a short, int, or long that is either 
      signed or unsigned. The method will also accept a string value. The method must be able to convert the value to 
      a positive, long number. For example, to pass the value as a long, set the variant type to 
      <b>VT_I4</b> and then set the <b>lVal</b> member of the variant to the 
      limit value.


## -returns



The method returns the following return values.




## -remarks



The following list lists the default limits for the 
     <a href="https://msdn.microsoft.com/225c583c-679c-43b4-85f4-3f2294fa7bc3">FsrmReportLimit</a> enumeration values used for 
     the <i>limit</i> parameter.

<table>
<tr>
<th>Limit</th>
<th>Default value</th>
</tr>
<tr>
<td><b>FsrmReportLimit_MaxDuplicateGroups</b></td>
<td>100 duplicate groups</td>
</tr>
<tr>
<td><b>FsrmReportLimit_MaxFiles</b></td>
<td>1,000 files</td>
</tr>
<tr>
<td><b>FsrmReportLimit_MaxFileGroups</b></td>
<td>10 groups</td>
</tr>
<tr>
<td><b>FsrmReportLimit_MaxFileScreenEvents</b></td>
<td>1,000 file screen events</td>
</tr>
<tr>
<td><b>FsrmReportLimit_MaxFilesPerDuplGroup</b></td>
<td>10 files per duplicate group</td>
</tr>
<tr>
<td><b>FsrmReportLimit_MaxFilesPerFileGroup</b></td>
<td>100 files per group</td>
</tr>
<tr>
<td><b>FsrmReportLimit_MaxFilesPerOwner</b></td>
<td>100 files per owner</td>
</tr>
<tr>
<td><b>FsrmReportLimit_MaxFilesPerPropertyValue</b></td>
<td>100 files per property</td>
</tr>
<tr>
<td><b>FsrmReportLimit_MaxOwners</b></td>
<td>10 owners</td>
</tr>
<tr>
<td><b>FsrmReportLimit_MaxPropertyValues</b></td>
<td>10 properties</td>
</tr>
<tr>
<td><b>FsrmReportLimit_MaxQuotas</b></td>
<td>1,000 quotas</td>
</tr>
<tr>
<td><b>FsrmReportLimit_MaxFolders</b></td>
<td>1,000 folders</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/308c5001-b84d-49ab-ae2c-f16466f9abca">FsrmReportManager</a>



<a href="https://msdn.microsoft.com/112ed457-1083-4550-abd6-933f4b128e9a">IFsrmReportManager</a>
 

 

