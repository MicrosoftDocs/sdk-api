---
UID: NF:strmif.IDvdControl2.SetDVDDirectory
title: IDvdControl2::SetDVDDirectory
author: windows-sdk-content
description: The SetDVDDirectory method sets the DVD drive that the DVD Navigator filter will read from.
old-location: dshow\idvdcontrol2_setdvddirectory.htm
old-project: DirectShow
ms.assetid: fa64a614-14cb-4ea9-a005-0e738490b6d6
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IDvdControl2 interface [DirectShow],SetDVDDirectory method, IDvdControl2.SetDVDDirectory, IDvdControl2::SetDVDDirectory, IDvdControl2SetDVDDirectory, SetDVDDirectory, SetDVDDirectory method [DirectShow], SetDVDDirectory method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_setdvddirectory, strmif/IDvdControl2::SetDVDDirectory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdControl2.SetDVDDirectory
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdControl2::SetDVDDirectory


## -description



The <code>SetDVDDirectory</code> method sets the DVD drive that the <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> filter will read from.




## -parameters




### -param pszwPath [in]

Pointer to a wide-character string that specifies the path of the root directory.


## -returns



Returns one of the following values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pszwPath</i> parameter points to an invalid DVD path, or a DVD drive is not found while enumerating.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The DVD Navigator is not initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
Invalid domain. For details, see Remarks.

</td>
</tr>
</table>
 




## -remarks



If <i>pszwPath</i> is <b>NULL</b>, the DVD Navigator tries to select a DVD volume on any available drive. On startup, the DVD Navigator automatically looks for a drive, starting at drive C, with a VIDEO_TS folder in the root folder. It is therefore only necessary to call <code>SetDVDDirectory</code> when you have more than one DVD drive on a machine, or if your DVD drive letter is A or B. When specifying the path, include the video_ts folder.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
SetDVDDirectory(L"e:\\video_ts");
</pre>
</td>
</tr>
</table></span></div>
Some DVD volumes may have their video in a directory named something other than "video_ts." The general idea is that an additional "DVD volume" (the set of .IFO. VOB, and .BUP files that would normally be stored in the VIDEO_TS directory) can be placed in a subdirectory on the disc. By changing the root to point to this directory, MSWebDVD will operate on this separate DVD volume. A new set of menus, titles, and so on will be available, independent of the titles in the VIDEO_TS root, which will no longer be accessible. Such directories are called "hidden directories." The following example shows how to set a hidden directory as the root, where "hidden" is a placeholder for whatever name the disc authors have given to the directory.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
SetDVDDirectory(L"d:\\webdvd\\hidden");
</pre>
</td>
</tr>
</table></span></div>
If the filter graph is running and the DVD Navigator finds a DVD in the directory specified by <i>pszwPath</i>, the DVD Navigator automatically begins playing the disc. This conforms with the DVD specification and ensures that the new disc is initialized properly. If you do not want the new disc to play automatically after <code>SetDVDDirectory</code> returns, you must set the DVD_ResetOnStop flag in <a href="https://msdn.microsoft.com/b3b28da8-b0cb-4d76-8184-93572e4b6d06">IDvdControl2::SetOption</a> to <b>TRUE</b> and stop the filter graph through a call to <a href="https://msdn.microsoft.com/89e48d43-a31f-4912-98ff-36ba2069812d">IMediaControl::Stop</a> on the Filter Graph Manager. If DVD_ResetOnStop is set to <b>FALSE</b>, then <code>SetDVDDirectory</code> returns VFW_E_DVD_INVALIDDOMAIN.

This method is demonstrated in the DVDSample application in <b>CDvdCore::SetDirectory</b>.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>
              Annex J Command Name
            </td>
<td>
              Valid Domains
            </td>
</tr>
<tr>
<td>None</td>
<td>DVD_DOMAIN_Stop</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2 Interface</a>
 

 

