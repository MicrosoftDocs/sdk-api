---
UID: NF:propsys.IPropertyStore.Commit
title: IPropertyStore::Commit (propsys.h)
description: After a change has been made, this method saves the changes.
helpviewer_keywords: ["Commit","Commit (IPropertyStore)","Commit method [Audio Devices]","Commit method [Audio Devices]","IPropertyStore interface","IPropertyStore interface [Audio Devices]","Commit method","IPropertyStore.Commit","IPropertyStore::Commit","audio.ipropertystore_commit","audio_syseffects_r_65453880-01ab-4b73-b766-bb1daeb863ba.xml","propsys/IPropertyStore::Commit"]
old-location: audio\ipropertystore_commit.htm
tech.root: audio
ms.assetid: a3cc6815-a16f-45e7-a2d5-8f354f712170
ms.date: 12/05/2018
ms.keywords: Commit, Commit (IPropertyStore), Commit method [Audio Devices], Commit method [Audio Devices],IPropertyStore interface, IPropertyStore interface [Audio Devices],Commit method, IPropertyStore.Commit, IPropertyStore::Commit, audio.ipropertystore_commit, audio_syseffects_r_65453880-01ab-4b73-b766-bb1daeb863ba.xml, propsys/IPropertyStore::Commit
req.header: propsys.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Available with Windows Vista and later versions of the Windows operating system.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Propsys.idl
req.dll: 
req.irql: All levels
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPropertyStore::Commit
 - propsys/IPropertyStore::Commit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.idl
 - Propsys.idl.dll
api_name:
 - IPropertyStore.Commit
---

# IPropertyStore::Commit


## -description

After a change has been made, this method saves the changes.



## -returns

The <code>IPropertyStore::Commit</code> method returns any one of the following:

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
All of the property changes were successfully written to the stream or path. This includes the case where no changes were pending when the method was called and nothing was written.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The stream or file is read-only; the method was not able to set the value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Some or all of the changes could not be written to the file. Another, more explanatory error can be used in place of E_FAIL.

</td>
</tr>
</table>

## -remarks

Before the <code>Commit</code> method returns, it releases the file stream or path that was initialized to be used by the method. Therefore, no <b>IPropertyStore</b> methods succeed after <code>Commit</code> returns. At that point, they return E_FAIL.

Property handlers must ensure that property changes result in a valid destination file, even if the <code>Commit</code> process terminates abnormally, or encounters any errors.

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>
