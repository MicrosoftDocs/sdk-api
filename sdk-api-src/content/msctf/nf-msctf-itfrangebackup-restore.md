---
UID: NF:msctf.ITfRangeBackup.Restore
title: ITfRangeBackup::Restore
author: windows-driver-content
description: ITfRangeBackup::Restore method
old-location: tsf\itfrangebackup_restore.htm
old-project: TSF
ms.assetid: bb168504-34c0-4d30-826e-61926fd10a2a
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITfRangeBackup interface [Text Services Framework],Restore method, ITfRangeBackup.Restore, ITfRangeBackup::Restore, Restore, Restore method [Text Services Framework], Restore method [Text Services Framework],ITfRangeBackup interface, _tsf_itfrangebackup_restore_ref, msctf/ITfRangeBackup::Restore, tsf.itfrangebackup_restore
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITfRangeBackup.Restore
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfRangeBackup::Restore


## -description




## -parameters




### -param ec [in]

Contains an edit cookie that identifies the edit session. This is the value passed to <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.


### -param pRange [in]

Pointer to an <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> object that receives the backup information. If this parameter is <b>NULL</b>, the backup information is restored into a copy of the range originally backed up by <b>ITfContext::CreateRangeBackup</b>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The context is not on a document stack.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The edit cookie specified by <i>ec</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pRange</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c3b52170-af1b-407b-9160-1265ae3c9afc">ITfContext::CreateRangeBackup
      </a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">
        ITfEditSession::DoEditSession
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">
        ITfRange
      </a>



<a href="https://msdn.microsoft.com/f98cd8d0-7033-4bd2-94a1-1a75913c2647">ITfRangeBackup</a>



<a href="ranges.htm">Ranges: Clones and Backups</a>
 

 

