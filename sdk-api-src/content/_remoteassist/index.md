---
UID: TP:remoteassist
ms.assetid: 0428476b-93a6-3bbc-b71e-e24fdda86703
ms.author: windowssdkdev
ms.date: 06/09/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
archived: true
---

# Remote Assistance

## -description

Overview of the Remote Assistance technology.

To develop Remote Assistance, you need these headers:

 * [rendezvoussession.h](../rendezvoussession/index.md)

For the programming guide, see [Remote Assistance](/previous-versions/windows/desktop/remoteassist).

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [__MIDL___MIDL_itf_rendezvoussession_0000_0000_0001 enumeration](..\rendezvoussession\ne-rendezvoussession-__midl___midl_itf_rendezvoussession_0000_0000_0001.md) | Provides the list of possible state codes of the session invitation. |
| [__MIDL___MIDL_itf_rendezvoussession_0000_0000_0002 enumeration](..\rendezvoussession\ne-rendezvoussession-__midl___midl_itf_rendezvoussession_0000_0000_0002.md) | Provides the list of possible flags for the session invitation. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IRendezvousApplication interface](..\rendezvoussession\nn-rendezvoussession-irendezvousapplication.md) | Exposes a method used by an instant messaging (IM) application to create a remote assistance session. |
| [IRendezvousSession interface](..\rendezvoussession\nn-rendezvoussession-irendezvoussession.md) | Exposes methods that send data about the session and that can terminate it. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IRendezvousApplication::SetRendezvousSession](..\rendezvoussession\nf-rendezvoussession-irendezvousapplication-setrendezvoussession.md) | Passes IRendezvousSession to the Windows Remote Assistance application. This method is used by the instant messaging application. |
| [IRendezvousSession::SendContextData](..\rendezvoussession\nf-rendezvoussession-irendezvoussession-sendcontextdata.md) | Sends the context data to the remote RendezvousApplication. |
| [IRendezvousSession::Terminate](..\rendezvoussession\nf-rendezvoussession-irendezvoussession-terminate.md) | Terminates the remote RendezvousApplication. |
| [IRendezvousSession::get_Flags](..\rendezvoussession\nf-rendezvoussession-irendezvoussession-get_flags.md) | Retrieves a value that indicates session information. For example, the session flag can indicate whether the user is the inviter or the invitee. |
| [IRendezvousSession::get_RemoteUser](..\rendezvoussession\nf-rendezvoussession-irendezvoussession-get_remoteuser.md) | Retrieves a pointer to a BSTR that contains the Windows Messenger contact name. |
| [IRendezvousSession::get_State](..\rendezvoussession\nf-rendezvoussession-irendezvoussession-get_state.md) | Retrieves a value that indicates the session state. |
