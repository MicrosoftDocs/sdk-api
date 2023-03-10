---
UID: NF:rdpappcontainerclient.IRemoteDesktopClientSettings.SetRdpProperty
title: IRemoteDesktopClientSettings::SetRdpProperty (rdpappcontainerclient.h)
description: Sets the value of a single named RDP property.
helpviewer_keywords: ["IRemoteDesktopClientSettings interface [Remote Desktop Services]","SetRdpProperty method","IRemoteDesktopClientSettings.SetRdpProperty","IRemoteDesktopClientSettings::SetRdpProperty","SetRdpProperty","SetRdpProperty method [Remote Desktop Services]","SetRdpProperty method [Remote Desktop Services]","IRemoteDesktopClientSettings interface","WinRTEncryptedPassword","WinRTPasswordEncoding","Workspace Id","administrative session","allow font smoothing","alternate full address","audiocapturemode","audiomode","authentication level","connection type","cookie based authentication server address","desktopheight","desktopwidth","disable full window drag","disable menu anims","disable themes","disable wallpaper","domain","enablecredsspsupport","full address","gatewaycredentialssource","gatewayhostname","gatewayprofileusagemethod","gatewayusagemethod","high resolution mouse","loadbalanceinfo","login web page address","pre-authentication server address","prompt for credentials","promptcredentialonce","rdpappcontainerclient/IRemoteDesktopClientSettings::SetRdpProperty","redirectclipboard","redirectprinters","require pre-authentication","support url","termserv.iremotedesktopclientsettings_setrdpproperty","use redirection server name","username"]
old-location: termserv\iremotedesktopclientsettings_setrdpproperty.htm
tech.root: TermServ
ms.assetid: 3c1a9e70-3e77-4f21-b3a1-8e4c3c5cf148
ms.date: 12/05/2018
ms.keywords: IRemoteDesktopClientSettings interface [Remote Desktop Services],SetRdpProperty method, IRemoteDesktopClientSettings.SetRdpProperty, IRemoteDesktopClientSettings::SetRdpProperty, SetRdpProperty, SetRdpProperty method [Remote Desktop Services], SetRdpProperty method [Remote Desktop Services],IRemoteDesktopClientSettings interface, WinRTEncryptedPassword, WinRTPasswordEncoding, Workspace Id, administrative session, allow font smoothing, alternate full address, audiocapturemode, audiomode, authentication level, connection type, cookie based authentication server address, desktopheight, desktopwidth, disable full window drag, disable menu anims, disable themes, disable wallpaper, domain, enablecredsspsupport, full address, gatewaycredentialssource, gatewayhostname, gatewayprofileusagemethod, gatewayusagemethod, high resolution mouse, loadbalanceinfo, login web page address, pre-authentication server address, prompt for credentials, promptcredentialonce, rdpappcontainerclient/IRemoteDesktopClientSettings::SetRdpProperty, redirectclipboard, redirectprinters, require pre-authentication, support url, termserv.iremotedesktopclientsettings_setrdpproperty, use redirection server name, username
req.header: rdpappcontainerclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsTscAx.dll
req.lib: 
req.dll: MsTscAx.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRemoteDesktopClientSettings::SetRdpProperty
 - rdpappcontainerclient/IRemoteDesktopClientSettings::SetRdpProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsTscAx.dll
api_name:
 - IRemoteDesktopClientSettings.SetRdpProperty
---

# IRemoteDesktopClientSettings::SetRdpProperty


## -description

Sets the value of a single named RDP property.

## -parameters

### -param propertyName [in]

A string that specifies the name of the property.

<div class="alert"><b>Note</b>  These string values are not case-sensitive.</div>
<div> </div>

The possible values are.





#### "administrative session" (Boolean)

Specifies whether the session is an administrative session. This can be one of the following values.





##### false

The session is not an administrative session.



##### True

The session is an administrative session.



#### "allow font smoothing" (Boolean)

Specifies whether font smoothing is allowed in the remote session. This can be one of the following 
         values.





##### false

Font smoothing is not allowed.



##### True

Font smoothing is allowed.



#### "alternate full address" (String)

Specifies an alternate name or IP address of the remote computer that you want to connect to.



#### "audiocapturemode" (Boolean)

Specifies the audio input capture mode. This can be one of the following values.





##### false

Do not capture audio input.



##### True

Capture audio input.



#### "audiomode" (Number)

Specifies where sounds are played. This can be one of the following values.





##### 0

Play sounds on the client computer.



##### 1

Play sounds on the host computer.



##### 2

Do not play sounds.



#### "authentication level" (Number)

Specifies the authentication level of the remote session. This can be one of the following values.





##### 0

None.



##### 1

Authentication required.



##### 2

Authentication negotiable.



##### 3

Authentication unspecified.



#### "connection type" (Number)

Specifies the connection type This can be one of the following values.





##### 1

Modem



##### 2

Low speed broadband



##### 3

Satellite



##### 4

High speed broadband



##### 5

WAN



##### 6

LAN



##### 7

Auto detect



#### "cookie based authentication server address" (String)

Specifies the address of the cookie-based authentication server.



#### "desktopheight" (Number)

Specifies the height, in pixels, of the virtual desktop.



#### "desktopwidth" (Number)

Specifies the width, in pixels, of the virtual desktop.



#### "disable full window drag" (Boolean)

Specifies whether showing window contents while dragging is disabled. This can be one of the following 
         values.





##### false

Enabled



##### True

Disabled



#### "disable menu anims" (Boolean)

Specifies whether showing menu animations is disabled. This can be one of the following values.





##### false

Enabled



##### True

Disabled



#### "disable themes" (Boolean)

Specifies whether themes are disabled. This can be one of the following values.





##### false

Enabled



##### True

Disabled



#### "disable wallpaper" (Boolean)

Specifies whether wallpapers are displayed. This can be one of the following values.





##### false

Wallpapers are displayed.



##### True

Wallpapers are not displayed.



#### "domain" (String)

Specifies the domain used to connect to the remote session.



#### "enablecredsspsupport" (Boolean)

Specifies whether to use CredSSP-based authentication for the remote session. This can be one of the 
         following values.





##### false

Do not use CredSSP-based authentication.



##### True

Use CredSSP-based authentication.



#### "full address" (String)

Specifies the address of the computer being connected to.



#### "gatewaycredentialssource" (Number)

Specifies the source for credentials for the Remote Desktop gateway. This can be one of the following 
         values.





##### 0

Prompt the user for their credentials and use NTLM authentication.



##### 1

Use a smart card for credentials.



##### 2

Use the credentials for the currently logged on user.



##### 3

Prompt the user for their credentials and use basic authentication.



##### 4

The user will select the credential source at logon.



##### 5

Use cookie-based authentication.



#### "gatewayhostname" (String)

Specifies the Remote Desktop gateway server name.



#### "gatewayprofileusagemethod" (Number)

Specifies the Remote Desktop gateway profile usage. This can be one of the following values.





##### 0

Use the gateway profile settings, if present.



##### 1

Use the explicit gateway settings, even if a gateway profile exists.



#### "gatewayusagemethod" (Number)

Specifies the Remote Desktop gateway usage. This can be one of the following values.





##### 0

Do not use a Remote Desktop gateway server. The <b>Bypass RD Gateway server for 
           local addresses</b> check box is cleared.



##### 1

Use the Remote Desktop gateway specified by the "gatewayhostname" property.



##### 2

Automatically detect the Remote Desktop gateway server settings.



##### 3

Use the default settings Remote Desktop gateway usage settings.



##### 4

Do not use a Remote Desktop gateway server. The <b>Bypass RD Gateway server for 
           local addresses</b> check box is selected.



#### "high resolution mouse" (Boolean)

Specifies the resolution mode for mouse input. This can be one of the following values.





##### false

Mouse input will be coalesced. Mouse data will be subsampled and sent according to the default 
           sampling rate.



##### True

Mouse input will not be coalesced. Mouse data will be sent at full resolution.



#### "loadbalanceinfo" (String)

Contains the load balancing cookie used to choose the best server for the client computer.



#### "login web page address" (String)

Specifies the address of the login webpage.



#### "pre-authentication server address" (String)

Specifies the address of the preauthentication server.



#### "prompt for credentials" (Boolean)

Specifies whether the user will be prompted for their credentials. This can be one of the following 
         values.





##### false

The user will not be prompted for credentials.



##### True

The user will be prompted for credentials.



#### "promptcredentialonce" (Number)

Specifies whether credential sharing for the Remote Desktop gateway is enabled. This can be one of the 
         following values.





##### 0

Credential sharing is disabled.



##### 1

Credential sharing is enabled.



#### "redirectclipboard" (Boolean)

Specifies whether the clipboard for the client is redirected to the remote session. This can be one of the 
         following values.





##### false

The clipboard is not redirected.



##### True

The clipboard is redirected.



#### "redirectprinters" (Boolean)

Specifies whether the printers for the client are redirected to the remote session. This can be one of the 
         following values.





##### false

The printers are not redirected.



##### True

The printers are redirected.



#### "require pre-authentication" (Number)

Specifies whether preauthentication is required. This can be one of the following values.





##### 0

Pre-authentication is not required.



##### 1

Pre-authentication is required.



#### "support url" (String)

Specifies the URL to obtain support information from.

<b>Boolean</b>



#### "use redirection server name" (Boolean)

Specifies whether a redirection server is allowed. This can be one of the following values.





##### false

A redirection server is not allowed.



##### True

A redirection server is allowed.



#### "username" (String)

Specifies the user name used to connect to the remote session.



#### "WinRTEncryptedPassword" (String)

Specifies an encrypted password. To set this property, you must perform the following actions.

<ol>
<li>Convert the clear text password to binary by using the 
          <a href="/uwp/api/windows.security.cryptography.cryptographicbuffer.convertstringtobinary">ConvertStringToBinary</a> 
          method on the <a href="/uwp/api/windows.security.cryptography.cryptographicbuffer">CryptographicBuffer</a> 
          class.</li>
<li>Set the <b>WinRTPasswordEncoding</b> property by using an equivalent value for the 
          encoding parameter you passed to the 
          <a href="/uwp/api/windows.security.cryptography.cryptographicbuffer.convertstringtobinary">ConvertStringToBinary</a> 
          method in step 1.</li>
<li>Call the 
          <a href="/uwp/api/Windows.Security.Cryptography.DataProtection.DataProtectionProvider">DataProtectionProvider(String)</a> 
          method by passing "LOCAL=user" for the input string.</li>
<li>Call the 
          <a href="/uwp/api/windows.security.cryptography.dataprotection.dataprotectionprovider.protectasync">ProtectAsync</a> 
          method to encrypt the binary string that contains the password.</li>
<li>Convert the 
          <a href="/uwp/api/windows.security.cryptography.cryptographicbuffer">CryptographicBuffer</a> object 
          returned by the 
          <a href="/uwp/api/windows.security.cryptography.dataprotection.dataprotectionprovider.protectasync">ProtectAsync</a> 
          method to a Base64 encoded value by using the 
          <a href="/uwp/api/windows.security.cryptography.cryptographicbuffer.encodetobase64string">EncodeToBase64String</a> 
          method.</li>
<li>Set this property (<b>WinRTEncryptedPassword</b>) with the Base64 encoded string 
          obtained in step 5.</li>
</ol>


#### "WinRTPasswordEncoding" (Number)

Specifies the type of encoding that can be applied to an encrypted password. This can be one of the 
         following values. The default value is 1. This property must be set before setting the 
         <b>WinRTEncryptedPassword</b> property.





##### 0

UTF8



##### 1

UTF16LE



##### 2

UTF16BE



#### "Workspace Id" (String)

Specifies the identifier of the RemoteApp and Desktop Connection workspace which this RDP file has been 
         published as part of.

### -param value [in]

The new property value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclientsettings">IRemoteDesktopClientSettings</a>