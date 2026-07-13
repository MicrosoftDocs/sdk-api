---
UID: NF:shobjidl.IPreviousVersionsInfo.AreSnapshotsAvailable
title: IPreviousVersionsInfo::AreSnapshotsAvailable (shobjidl.h)
description: Queries for the availability of a Windows Server 2003 volume image recorded by the system at an earlier time.
helpviewer_keywords: ["AreSnapshotsAvailable","AreSnapshotsAvailable method [Windows Shell]","AreSnapshotsAvailable method [Windows Shell]","IPreviousVersionsInfo interface","FALSE","IPreviousVersionsInfo interface [Windows Shell]","AreSnapshotsAvailable method","IPreviousVersionsInfo.AreSnapshotsAvailable","IPreviousVersionsInfo::AreSnapshotsAvailable","TRUE","_shell_IPreviousVersionsInfo_AreSnapshotsAvailable","shell.IPreviousVersionsInfo_AreSnapshotsAvailable","shobjidl/IPreviousVersionsInfo::AreSnapshotsAvailable"]
old-location: shell\IPreviousVersionsInfo_AreSnapshotsAvailable.htm
tech.root: shell
ms.assetid: 03a0b218-4683-42b2-9080-9b92701dff1e
ms.date: 12/05/2018
ms.keywords: AreSnapshotsAvailable, AreSnapshotsAvailable method [Windows Shell], AreSnapshotsAvailable method [Windows Shell],IPreviousVersionsInfo interface, FALSE, IPreviousVersionsInfo interface [Windows Shell],AreSnapshotsAvailable method, IPreviousVersionsInfo.AreSnapshotsAvailable, IPreviousVersionsInfo::AreSnapshotsAvailable, TRUE, _shell_IPreviousVersionsInfo_AreSnapshotsAvailable, shell.IPreviousVersionsInfo_AreSnapshotsAvailable, shobjidl/IPreviousVersionsInfo::AreSnapshotsAvailable
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Twext.dll (version 5.2 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPreviousVersionsInfo::AreSnapshotsAvailable
 - shobjidl/IPreviousVersionsInfo::AreSnapshotsAvailable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Twext.dll
api_name:
 - IPreviousVersionsInfo.AreSnapshotsAvailable
---

# IPreviousVersionsInfo::AreSnapshotsAvailable


## -description

Queries for the availability of a Windows Server 2003 volume image recorded by the system at an earlier time.

## -parameters

### -param pszPath [in]

Type: <b>LPCWSTR</b>

A null-terminated Unicode string containing the fully qualified path to a file or folder on the volume in question.




<div class="alert"><b>Note</b>  Only paths to files and folders stored on a Windows Server 2003 volume are currently supported.
          </div>
<div> </div>

### -param fOkToBeSlow [in]

Type: <b>BOOL</b>

A boolean value specifying whether a server should be contacted to determine the availability of stored volume images. For more details, see the Remarks section.



#### TRUE

Contact the server if the results are not already cached.



#### FALSE

Do not contact the server. Use cached results instead.

### -param pfAvailable [out]

Type: <b>BOOL*</b>

A pointer to a boolean variable containing the result. This value is valid only if the method call succeeds; otherwise, it is undefined.



#### TRUE

At least one stored image of the volume where the file or folder named in <i>pszPath</i> resides is available.



#### FALSE

No volume images are stored.

## -returns

Type: <b>HRESULT</b>

Returns standard error values, including, but not limited to, the following:

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
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
<i>fOkToBeSlow</i> is <b>FALSE</b> and the result is not currently cached.

</td>
</tr>
</table>

## -remarks

If <b>IPreviousVersionsInfo::AreSnapshotsAvailable</b> is called on a file or folder, the result does not indicate that rollback information is available for that specific file or folder, merely that a snapshot of the entire volume is available. This result is cached and subsequent calls inquiring about anything stored on that same volume access the cached results—with little performance overhead—instead of recontacting the server.

Once the server's response is cached in memory, subsequent calls do not contact the server even if <i>fOkToBeSlow</i> is <b>TRUE</b>. If <i>fOkToBeSlow</i> is <b>FALSE</b> and the server's response is not already cached from a previous call, the method returns E_PENDING. In that case, set <i>fOkToBeSlow</i> to <b>TRUE</b> and call <b>IPreviousVersionsInfo::AreSnapshotsAvailable</b> again to contact the server.

For better performance, a UI thread calling this method should always set <i>fOkToBeSlow</i> to <b>FALSE</b>. If the method returns E_PENDING, follow these steps.

                

<ul>
<li>Create another instance of <a href="/windows/desktop/api/shobjidl/nn-shobjidl-ipreviousversionsinfo">IPreviousVersionsInfo</a> on a background thread.</li>
<li>Call <b>IPreviousVersionsInfo::AreSnapshotsAvailable</b> with <i>fOkToBeSlow</i> set to <b>TRUE</b>.</li>
<li>Signal the original UI thread to call <b>IPreviousVersionsInfo::AreSnapshotsAvailable</b> again. The results are then pulled from the cache.</li>
</ul>
