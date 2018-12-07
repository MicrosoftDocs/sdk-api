---
UID: NF:icm.OpenColorProfileW
title: OpenColorProfileW function
author: windows-sdk-content
description: The OpenColorProfile function creates a handle to a specified color profile. The handle can then be used in other profile management functions.
old-location: wcs\opencolorprofile.htm
tech.root: WCS
ms.assetid: 5f738012-690f-4ff9-bc40-4ccbd47169c6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CREATE_ALWAYS, CREATE_NEW, FILE_SHARE_READ, FILE_SHARE_WRITE, OPEN_ALWAYS, OPEN_EXISTING, OpenColorProfile, OpenColorProfile function [Windows Color System], OpenColorProfileA, OpenColorProfileW, PROFILE_READ, PROFILE_READWRITE, TRUNCATE_EXISTING, _color_OpenColorProfile, icm/OpenColorProfile, icm/OpenColorProfileA, icm/OpenColorProfileW, wcs.opencolorprofile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: icm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OpenColorProfileW (Unicode) and OpenColorProfileA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mscms.lib
req.dll: Mscms.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mscms.dll
api_name:
 - OpenColorProfile
 - OpenColorProfileA
 - OpenColorProfileW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- OpenColorProfileW
: 
---

# OpenColorProfileW function


## -description


The <b>OpenColorProfile</b> function creates a handle to a specified color profile. The handle can then be used in other profile management functions.


## -parameters




### -param pProfile

Pointer to a color profile structure specifying the profile. The <i>pProfile</i> pointer can be freed as soon as the handle is created.


### -param dwDesiredAccess

Specifies how to access the given profile. This parameter must take one the following constant values.<div> </div>


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PROFILE_READ"></a><a id="profile_read"></a><dl>
<dt><b>PROFILE_READ</b></dt>
</dl>
</td>
<td width="60%">
Opens the profile for read access.

</td>
</tr>
<tr>
<td width="40%"><a id="PROFILE_READWRITE"></a><a id="profile_readwrite"></a><dl>
<dt><b>PROFILE_READWRITE</b></dt>
</dl>
</td>
<td width="60%">
Opens the profile for both read and write access. Has no effect for WCS XML profiles.

</td>
</tr>
</table>
 


### -param dwShareMode

Specifies how the profile should be shared, if the profile is contained in a file. A value of zero prevents the profile from being shared at all. The parameter can contain one or both of the following constants (combined by addition or logical OR).<div> </div>


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_SHARE_READ"></a><a id="file_share_read"></a><dl>
<dt><b>FILE_SHARE_READ</b></dt>
</dl>
</td>
<td width="60%">
Other open operations can be performed on the profile for read access.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SHARE_WRITE"></a><a id="file_share_write"></a><dl>
<dt><b>FILE_SHARE_WRITE</b></dt>
</dl>
</td>
<td width="60%">
Other open operations can be performed on the profile for write access. Has no effect for WCS XML profiles.

</td>
</tr>
</table>
 


### -param dwCreationMode

Specifies which actions to take on the profile while opening it, if it is contained in a file. This parameter must take one of the following constant values.<div> </div>


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CREATE_NEW"></a><a id="create_new"></a><dl>
<dt><b>CREATE_NEW</b></dt>
</dl>
</td>
<td width="60%">
Creates a new profile. Fails if the profile already exists.

</td>
</tr>
<tr>
<td width="40%"><a id="CREATE_ALWAYS"></a><a id="create_always"></a><dl>
<dt><b>CREATE_ALWAYS</b></dt>
</dl>
</td>
<td width="60%">
Creates a new profile. Overwrites the profile if it exists.

</td>
</tr>
<tr>
<td width="40%"><a id="OPEN_EXISTING"></a><a id="open_existing"></a><dl>
<dt><b>OPEN_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
Opens the profile. Fails if it does not exist

</td>
</tr>
<tr>
<td width="40%"><a id="OPEN_ALWAYS"></a><a id="open_always"></a><dl>
<dt><b>OPEN_ALWAYS</b></dt>
</dl>
</td>
<td width="60%">
Opens the profile if it exists. For ICC profiles, if the profile does not exist, creates the profile. For WCS XML profiles, if the profile does not exist, returns an error.

</td>
</tr>
<tr>
<td width="40%"><a id="TRUNCATE_EXISTING"></a><a id="truncate_existing"></a><dl>
<dt><b>TRUNCATE_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
Opens the profile, and truncates it to zero bytes, returning a blank ICC profile. Fails if the profile doesn't exist.

</td>
</tr>
</table>
 


## -returns



If this function succeeds, the return value is the handle of the color profile that is opened. For ICC and WCS profiles, a CAMP and GMMP are provided by the function based on the current default CAMP and GMMP in the registry.

When OpenColorProfile encounters an ICC profile with an embedded WCS profile, and if the dwType member within the Profile structure does not take the value DONT_USE_EMBEDDED_WCS_PROFILES, it should extract and use the WCS profile(s) contained in this WcsProfilesTag. The HPROFILE returned would be a WCS HPROFILE.

If this function fails, the return value is <b>NULL</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



If the profile data is not specified using a file name, <i>dwShareMode</i> and <i>dwCreationMode</i> are ignored.

<i>dwCreationMode</i> flags CREATE_NEW, CREATE_ALWAYS, and TRUNCATE_EXISTING, will always return blank ICC HPROFILEs. If other <i>dwCreationMode</i> flags are present, InternalOpenColorProfile is called (using the flags as provided by the API) to determine whether the profile is ICC or WCS XML.

Within the ICC code path, an ICC HPROFILE is returned using the requested sharing, access and creation flags as specified in the tables above.

Within the WCS path, the <i>dwCreationMode</i> flag OPEN_ALWAYS will fail if the profile doesn't exist, since WCS profiles cannot be created or edited within the WCS architecture (they must be edited outside of it, using MSXML6). For the same reason, <i>dwShareMode</i> flag FILE_SHARE_WRITE, and <i>dwDesiredAccess</i> flag PROFILE_READWRITE are ignored within the WCS path.

When the function opens the ICC profile, it will look for a <i>WcsProfilesTag</i> and, if there is one, it will extract and use the original WCS profiles contained therein. (See <a href="https://msdn.microsoft.com/6e9aaad6-a7d4-4685-b694-89d499a411e1">WcsCreateIccProfile</a>.)

An HPROFILE with WCS profile information is derived from a DMP by acquiring the default CAMP and default GMMP from the registry. An HPROFILE is a composition of a DMP, CAMP and GMMP.

Once the handle to the color profile is created, any information used to create that handle can be deleted.

Use the <a href="https://msdn.microsoft.com/49656afa-64fc-4421-8948-34a65c9f829e">CloseColorProfile</a> function to close an object handle returned by <b>OpenColorProfile</b>.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/49656afa-64fc-4421-8948-34a65c9f829e">CloseColorProfile</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/e7f50d1a-3756-4da2-96ea-f9a5e1958be5">PROFILE</a>
 

 

