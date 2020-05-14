---
UID: NF:strmif.IDvdControl2.Resume
title: IDvdControl2::Resume (strmif.h)
description: The Resume method leaves a menu and resumes playback.helpviewer_keywords: ["IDvdControl2 interface [DirectShow]","Resume method","IDvdControl2.Resume","IDvdControl2::Resume","IDvdControl2Resume","Resume","Resume method [DirectShow]","Resume method [DirectShow]","IDvdControl2 interface","dshow.idvdcontrol2_resume","strmif/IDvdControl2::Resume"]
old-location: dshow\idvdcontrol2_resume.htm
tech.root: DirectShow
ms.assetid: 522dcb38-8c17-46b0-b5aa-5ee380057077
ms.date: 12/05/2018
ms.keywords: IDvdControl2 interface [DirectShow],Resume method, IDvdControl2.Resume, IDvdControl2::Resume, IDvdControl2Resume, Resume, Resume method [DirectShow], Resume method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_resume, strmif/IDvdControl2::Resume
f1_keywords:
- strmif/IDvdControl2.Resume
dev_langs:
- c++
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IDvdControl2.Resume
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl2::Resume


## -description



The <code>Resume</code> method leaves a menu and resumes playback.




## -parameters




### -param dwFlags [in]

Bitwise OR of one or more flags from the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_cmd_flags">DVD_CMD_FLAGS</a> enumeration, specifying how to synchronize the command.


### -param ppCmd [out]

Receives a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcmd">IDvdCmd</a> object that can be used to synchronize DVD commands. The caller must release the interface. This parameter can be <b>NULL</b>. For more information, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/synchronizing-dvd-commands">Synchronizing DVD Commands</a>.


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
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
UOP control prohibits the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_NO_RESUME_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
Resume was called from the Video Manager Menu.

</td>
</tr>
</table>
 




## -remarks



This method returns to playback from the location where play left off.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

This method is demonstrated in the DVDSample application in <b>CDvdCore::RootMenu</b> and <b>CDvdCore::TitleMenu</b>.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>Resume</td>
<td>
<ul>
<li>DVD_DOMAIN_VideoManagerMenu</li>
<li>DVD_DOMAIN_VideoTitleSetMenu</li>
<li>DVD_DOMAIN_Stop</li>
</ul>
</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>
 

 

