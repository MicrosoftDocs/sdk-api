---
UID: NF:sfc.SfcIsKeyProtected
title: SfcIsKeyProtected function (sfc.h)
description: Determines whether the specified registry key is protected.
helpviewer_keywords: ["KEY_WOW64_32KEY","KEY_WOW64_64KEY","SfcIsKeyProtected","SfcIsKeyProtected function [Setup API]","setup.sfciskeyprotected","sfc/SfcIsKeyProtected"]
old-location: setup\sfciskeyprotected.htm
tech.root: setup
ms.assetid: 6e26a539-a22a-487a-b720-fa3660c1b485
ms.date: 12/05/2018
ms.keywords: KEY_WOW64_32KEY, KEY_WOW64_64KEY, SfcIsKeyProtected, SfcIsKeyProtected function [Setup API], setup.sfciskeyprotected, sfc/SfcIsKeyProtected
req.header: sfc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Sfc.lib
req.dll: Sfc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SfcIsKeyProtected
 - sfc/SfcIsKeyProtected
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Sfc.dll
api_name:
 - SfcIsKeyProtected
---

# SfcIsKeyProtected function


## -description

Determines whether the specified registry key is protected. Applications should avoid replacing protected registry keys.

## -parameters

### -param KeyHandle [in]

A handle to the root registry key. This must be a handle to one of the following <a href="/windows/desktop/SysInfo/predefined-keys">predefined keys</a>.

<p class="indent">HKEY_CLASSES_ROOT

<p class="indent">HKEY_CURRENT_USER

<p class="indent">HKEY_LOCAL_MACHINE

<p class="indent">HKEY_USERS

### -param SubKeyName [in, optional]

A <b>null</b>-terminated string value containing the name of the subkey. This key must a subkey of the key identified by the <i>hKey</i> parameter. For more information about key names, see <a href="/windows/desktop/SysInfo/structure-of-the-registry">Structure of the Registry</a>. 
If this parameter is <b>NULL</b>, the function only checks whether the root registry key is protected.

### -param KeySam [in]

A constant that specifies the alternate registry view that should be used by applications that run on 64-bit Windows.  This flag is ignored on the x86 platform. For more information, see <a href="/windows/desktop/WinProg64/accessing-an-alternate-registry-view">Accessing an Alternate Registry View</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x0000</dt>
</dl>
</td>
<td width="60%">
Use the 32-bit registry key from 32-bit applications and use the 64-bit registry key from 64-bit applications.

</td>
</tr>
<tr>
<td width="40%"><a id="KEY_WOW64_64KEY"></a><a id="key_wow64_64key"></a><dl>
<dt><b>KEY_WOW64_64KEY</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
Use the 64-bit registry key from either a 32-bit or 64-bit application.

</td>
</tr>
<tr>
<td width="40%"><a id="KEY_WOW64_32KEY"></a><a id="key_wow64_32key"></a><dl>
<dt><b>KEY_WOW64_32KEY</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
Use the 32-bit registry key from either a 32-bit or 64-bit application.

</td>
</tr>
</table>

## -returns

If the key is protected, the return value is a nonzero value.

If the key is not protected, the return value is zero.

## -remarks

A key is protected by WRP if the path exists and is protected by WRP. The <b>SfcIsKeyProtected</b> function indicates that a subkey is protected by WRP if the subkey has a  parent key that is protected by WRP.  

For example, if the following registry key exists on the system and is protected by WRP:


<pre><b>HKEY_LOCAL_MACHINE</b>
   <b>SOFTWARE</b>
      <b>Classes</b>
         <b>Microsoft</b>
            <b>&lt;WinFeature&gt;</b></pre>


The <b>SfcIsKeyProtected</b> function returns a nonzero value for the following subkey. The new subkey does not need to exist for the function to determine that it is WRP-protected.


<pre><b>HKEY_LOCAL_MACHINE</b>
   <b>SOFTWARE</b>
      <b>Classes</b>
         <b>Microsoft</b>
            <b>&lt;WinFeature&gt;</b>
               <b>&lt;new subkey&gt;</b></pre>

## -see-also

<a href="/windows/desktop/api/sfc/nf-sfc-sfcisfileprotected">SfcIsFileProtected</a>
