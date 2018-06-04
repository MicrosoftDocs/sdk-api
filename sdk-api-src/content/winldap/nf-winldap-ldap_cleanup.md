---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# ldap_cleanup function


## -description



<div class="alert"><b>Warning</b>  <p class="note">The <b>ldap_cleanup</b> function may cause unpredictable 
      behavior at DLL unload time so, there is no way to safely clean up resources when dynamically loading and 
      unloading the wldap32.dll.

<p class="note">Because of this, resource leaks can occur on unload of the library. Use of 
      <b>ldap_cleanup</b> is therefore not recommended and, is at 
      your own risk.

</div>
<div> </div>



## -parameters




### -param hInstance

This parameter is ignored.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see 
       <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa367014(v=vs.85).aspx">Return Values</a>.




## -remarks



<div class="alert"><b>Warning</b>  The <b>ldap_cleanup</b> function may cause 
    unpredictable behavior at the DLL unload time.  Use is not recommended and is at your own risk.</div>
<div> </div>


